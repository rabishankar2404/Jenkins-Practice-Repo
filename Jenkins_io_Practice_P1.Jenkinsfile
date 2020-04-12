
#------------------------Creating your first Pipeline-----------------------
Pipeline {
    agent { docker {image 'maven:3.3.3'}}

    Stages{
        stage('Build Java App') {
            steps{
             sh 'maven --verion'
            }
        }
    }
}
#-------------------------------------------------------------
#Node App

Pipeline {
    agent {docker {image 'node 6.3'}}
    
    Stages {
        stage ('Build None Aap'){
            steps {
             sh 'npm --verison'
            }
        }
    }
}

#-------------------------------------------------------------
#Python App

Pipeline {
    agent {docekr {image 'python:3.5.1'}}

    Stages{
        stage ('Build Python App'){
            steps {
                sh 'python --verion'
            }
        }
    }
}
    
#------------------------------------------------------------
# PHP App

Pipeline {
    agent {docker {Image 'php'}}

    Stages {
        stage ('Build Php App') {
            steps {
                sh 'Php --verison'
            }
        }   
    }
}

#-------------------------------------------------------------
# Go App
Pipeline{
    agent {docker { image 'golang '}}

    Stages{
        stage ('Build Go App') {
           steps {
            sh 'go verison'
           }
        }
    } 
}

#-----------------------------------------------END----------------
