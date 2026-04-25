pipeline {
    agent { label 'docker-agent' }
    
    parameters {
        booleanParam(name: 'RUN_TESTS', defaultValue: true, description: 'Check this box to run the Test stage')
    }
    
    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
            }
        }
        stage('Test') {
            when {
                expression { return params.RUN_TESTS }
            }
            steps {
                echo 'Tests are running because the box was checked!'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
            }
        }
    }
}
