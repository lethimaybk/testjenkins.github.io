pipeline {
    agent any
    
    stages {
        stage('Clone git') {
            steps {
                sh 'git clone https://github.com/lethimaybk/testjenkins.github.io.git;\
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