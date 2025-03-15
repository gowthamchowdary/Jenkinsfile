pipeline {
  agent any
          stages{
            stage('one'){
              steps{
                hi this is gowtham
              }
            }
            stage('two'){
              steps{
                input('do you want to proceed')
              }
            }
            stage('three) {
                    when{
                      not{
                        branch "main"
                      }
                    }
                  steps{
                    echo "hello"
                  }
                  }
                  stage('four'){
                    parallel{
                      stage('unit Test'){
                        steps{
                          echo "running the unit test"
                        }
                      }
                      stage('integration test'){
                        agent{
                          docker{
                            reuseNode false
                            image 'ubuntu'
                          }
                        }
                        steps{
                          echo "running integration test"
                        }
                      }
                    }
                  }
              
