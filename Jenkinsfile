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
                def workspace = pwd()
                sh "docker run --rm -v ${workspace}:/src -v /data:/data netroby/alpine-rsync rsync -avzP /src/* /data/www/oneway.netroby.com/"                
            }
        }
    }
}

