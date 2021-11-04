pipeline {
    agent any
    environment {
        BUILD_SCRIPTS_GIT="https://github.com/lethimaybk/testjenkins.github.io.git"

    }
    stages {
        stage('Clone git') {
            steps {
                sh 'git clone $BUILD_SCRIPTS_GIT;\
                    git add .;\
                    git commit -m "modified";\
                    git push origin main'
            }
        }

        stage('Build') {
            steps {
                echo 'Building....'
            }
        }
        stage('Run') {
            steps {
                sh 'python3 testjenkins.py'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing....'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}