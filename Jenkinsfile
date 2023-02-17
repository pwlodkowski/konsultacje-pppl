
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
    //def scannerHome = tool 'SonarQScanner';
    withSonarQubeEnv('SonarQ') { // If you have configured more than one global server connection, you can specify its name
      //sh "${scannerHome}/bin/sonar-scanner"
        //println ${env.SONAR_HOST_URL} 
    }
  }
}

