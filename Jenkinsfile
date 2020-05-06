pipeline {
         agent any
         environment { 
        CC = 'clang'
    }
         stages {
                 stage('One') {
                 steps {
                          echo "Hi, this is Zulaikha from edureka"
                          echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL} node ${env.NODE_NAME}".${CC}
                          
                 }
                 }
                 stage('Two') {
                          
                 steps {
                    input('Do you want to proceed?')
                 }
                 }
                 stage('Three') {
                 when {
                       not {
                            branch "master"
                       }
                 }
                       steps{
                          echo "hello"
                          }         
                              
            }
            steps {
                echo "when condition test"
            }
                 }
                 }
                 stage('Four') {
                 parallel { 
                            stage('Unit Test') {
                           steps {
                                echo "Running the unit test..."
                           }
                           }
                            stage('Integration test') {
                           
                              steps {
                                echo "Running the integration test..."
                              }
                           }
                           }
                           }
              }
}
