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
                sh "docker run --rm -v $(pwd):/src -v /data:/data netroby/alpine-rsync rsync -avzP /src/* /data/www/oneway.netroby.com/"                
            }
        }
    }
}

