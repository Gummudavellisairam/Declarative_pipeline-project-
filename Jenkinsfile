pipeline {
         agent any
                stages {
                       stage('one') {
                               steps {
                                        echo 'Hi this is the stage one'
                               }
                        }
                        stage('two') {
                                steps {
                                         input('Do you want to proceed or not?')
                                }
                        }
                        stage('three') {
                                 when {
                                         not {
                                                 branch "master"
                                         }
                                  }
                                  steps {
                                          echo "Hello"
                                  }
                         }
                         stage('four') {
                                          parallel {
                                                stage('Unit test') {
                                                                    steps {
                                                                            echo "Running unit test...."
                                                                     }
                                                 stage('Integration test') {
                                                                     steps { 
                                                                             echo "running Integration testing...."
                                                                           }
                                             }
                                         }
                  }
            }      
                         
