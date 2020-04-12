
#--------------------------------------Running multiple Steps-------------------------------------------
#Linux, BSD, and Mac OS

Pipeline {
    agent any 

    Stages {
        stage ('Build') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "multiple shell steps work too"
                    ls -lah
                '''
            }
        }
    }
}


#--------------------------------------

pipeline{
    agent any 

    stages {
        stage ('Deploy') {
            steps  {
                retry(3) {
                    sh './flakey-deploy.sh'
                }

                timeout( time: 3,unit: 'Minutes'){
                    sh './Healt-check.sh'
                }
            }
        }
    }
}

-------------------------------------

pipeline{
    
    agent any 
     stages {
         stages ('Test') {
             steps {
                 sh 'echo "Fail!"; exit 1'
             }
         }
     }
     post{
          always{
              echo "This will Always Run"
          }
          success{
              echo "This will run only Sucessful"
          }
          failure {
              echo "This will run only if failed"
          }
          unstable {
              echo " This will run only if build was marked as unstable"
          }
          changed{
              echo " This will run only if the state of the pipeline changed"
              echo " For example , if the pipeline was previously failing but now sucessful"
                        }
     }
}