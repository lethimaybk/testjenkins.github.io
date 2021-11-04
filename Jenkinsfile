pipeline {
    agent any
    enviroment {
        BUILD_SCRIPTS_GIT="https://github.com/lethimaybk/testjenkins.github.io.git"
        BUILD_SCRIPT="mypipeline"
    }
    stages {
        stage('Clone git') {
            steps {
                sh 'mkdir -p $WORKSPACE/repo;\
                    git clone $BUILD_SCRIPTS_GIT repo/$BUILD_SCRIPT;\
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