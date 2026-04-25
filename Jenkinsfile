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
            when {
                branch 'main' // This stage ONLY runs if we are on the main branch
            }
            steps {
                echo 'Running tests on the main branch...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    post {
        always {
            echo 'I run regardless of success or failure (good for cleanup).'
        }
        success {
            echo 'The build passed! Moving to the next step.'
        }
    }
}
