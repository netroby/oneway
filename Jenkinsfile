pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                sh "cp -TRv ./ /data/www/oneway.netroby.com/"                
                sh "rm -rf /data/www/oneway.netroby.com/.git"
            }
        }
    }
}

