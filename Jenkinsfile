pipeline {
      agent { dockerfile true }
      stage('SonarQube analysis') {

            environment {

                scannerHome = tool 'sonar_scanner'

            }

            steps {

                script{

                    echo '=========== SonarQube analysis ============'

                    withSonarQubeEnv('SonarQube') {

                        sh '${scannerHome}/bin/sonar-scanner --version'

                    }

                }

      }
}
