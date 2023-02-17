pipeline {
    agent any

    stages {
        stage('Analize') {
            steps {
                echo 'Analize ...'
            }
        }
        stage('Build') {
            steps {
                echo 'Building ...'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing ...'
            }
        }
        stage('Deploy Stage') {
            steps {
                echo 'Deploying ...'
            }
        }
        stage('Deploy Prod') {
            steps {
                echo ' Deploing prod ...'
                }
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
