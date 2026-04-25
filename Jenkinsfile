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
            echo 'Post build condition running: I am finished with the work!' [cite: 54]
        }
        failure { 
            echo 'Post Action: The build has failed.' [cite: 54]
        }
    }
}
