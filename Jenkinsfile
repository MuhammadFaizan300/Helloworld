
flag = true

pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building Project...'
            }
        }
        stage('Test') {
            when { 
                expression { flag == true }
            }
            steps {
                echo 'Testing Project...'
            }
        }
    }
}
