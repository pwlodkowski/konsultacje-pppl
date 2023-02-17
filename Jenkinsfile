
pipeline {
    agent any

    stages {
        stage('SonarQube analysis') {
            def scannerHome = tool 'SonarScanner 4.0';
            withSonarQubeEnv('My SonarQube Server') { // If you have configured more than one global server connection, you can specify its name
            sh "${scannerHome}/bin/sonar-scanner"
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


node {
  stage('SonarQ') {
    def scannerHome = tool 'SonarQScanner';
    withSonarQubeEnv() {
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}

