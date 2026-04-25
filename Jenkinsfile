pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building Project...'
            }
        }
    }
    post { 
        always { 
            echo 'Post build condition running'
        }
        failure { 
            echo 'Post Action if Build Failed'
        }
    }
}
