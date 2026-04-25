pipeline {
    agent { label 'docker-agent' }
    tools {
        maven 'maven-3.9' // Tells Jenkins to download and provide Maven to the Agent
    }
    environment {
        APP_NAME = 'MyJavaApp'
        VERSION = '1.1.0'
    }
    stages {
        stage('Initialize') {
            steps {
                echo "Starting build for ${env.APP_NAME} version ${env.VERSION}"
                sh 'mvn --version' // Verifies Maven was installed by Jenkins
            }
        }
    }
}
