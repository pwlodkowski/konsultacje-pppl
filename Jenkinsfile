
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
        sh "sonar-scanner \
            -Dsonar.projectKey=konsultacje-opl \
            -Dsonar.sources=. \
            -Dsonar.host.url=http://localhost:9000 \
            -Dsonar.login=sqp_9c52e5e35efbc3b2e49eb9f21e89dbc577db3455"
        println "${env.SONAR_HOST_URL}"
        println "${env.SONAR_CONFIG_NAME}"
        println "${env.SONAR_AUTH_TOKEN}"
    }
  }
}

