pipeline {
    agent any
    environment {
    BUILD_SCRIPTS_GIT="https://github.com/lethimaybk/testjenkins.github.io.git"
    BUILD_SCRIPTS='mypipeline'
    BUILD_HOME='/var/lib/jenkins/workspace'
    }
    stages {
        stage('Checkout: Code') {
          steps {
            sh "mkdir -p $WORKSPACE/repo;\
                git clone $BUILD_SCRIPTS_GIT repo/$BUILD_SCRIPTS"
            sh "chmod -R +x $WORKSPACE/repo/$BUILD_SCRIPTS"
            }
        }

        stage('Build') {
            steps {
                echo 'Build tu dong duoc roi ne'
            }
        }

        stage('Test') {
            steps {
                echo 'Tested'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployed'
            }
        }
    }
}
