pipeline {
    agent any

    parameters {
        string(name: 'VERSION_TO_DEPLOY', defaultValue: '1.1.0', description: 'Enter the version for deployment')
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Check this box to run tests')
    }

    environment {
        NEW_VERSION = '1.3.0'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building Project...'
                echo "Building version ${NEW_VERSION}"
            }
        }

        stage('Test') {
            when {
                expression { params.executeTests == true }
            }
            steps {
                echo 'Testing Project...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Project...'
                echo "Deploying version ${params.VERSION_TO_DEPLOY}"
            }
        }
    }

    post {
        always {
            echo 'Task is complete!'
        }
    }
}     
