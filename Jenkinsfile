pipeline {
    agent { label 'docker-agent' } 
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'java -version' 
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
            }
        }
    }
}
