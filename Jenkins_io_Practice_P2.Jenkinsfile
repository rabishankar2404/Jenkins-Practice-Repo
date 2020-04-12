
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