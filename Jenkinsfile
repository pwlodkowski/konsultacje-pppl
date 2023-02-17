pipeline {
    agent any

    stages {
        stage('Analize') {
            steps {
                echo 'Analize..'
                sh "~/Workspace/konsultacje-pppl/sonar.sh"
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
