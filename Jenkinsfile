pipeline {
         agent any
        
         stages {
                 stage('One') {
                 steps {
                          echo "Hi, this is Zulaikha from edureka"
                     echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL} node ${env.NODE_NAME}"
                          
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
                          
                          steps {
                      when {
              expression {
                currentBuild.result == null || currentBuild.result == 'SUCCESS' 
              }
             }
                                   steps{
                                   echo "helo"
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
