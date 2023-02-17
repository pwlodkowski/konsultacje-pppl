## ------------
## Normal Stage
## ------------
pipeline {
    agent { label 'test' }
    stages {
        stage('Build') {
            steps {
                sh 'echo "building your code"'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "testing your code"'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "approval required"'
                sh 'echo "deploying your code"'
            }
        }
    }
}
