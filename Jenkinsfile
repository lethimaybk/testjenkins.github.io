pipeline {
    agent any
    stages {
        stages {
            steps('Build') {
                echo "Building..."
            }
        }
        stages('Test') {
            steps {
                echo 'Testing...'
            }
        }
        stages('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}