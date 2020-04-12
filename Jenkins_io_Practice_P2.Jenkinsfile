
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
