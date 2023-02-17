
pipeline {
    agent any

    stages {
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


node {
  stage('SonarQube analysis') {
    def scannerHome = tool 'SonarQScaner';
    withSonarQubeEnv('SonarQScaner') { // If you have configured more than one global server connection, you can specify its name
        sh "sonar-scanner"
        println "${env.SONAR_HOST_URL}"
        println "${env.SONAR_CONFIG_NAME}"
        println "${env.SONAR_AUTH_TOKEN}"
    }
  }
}

