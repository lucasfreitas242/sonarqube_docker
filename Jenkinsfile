pipeline {
  agent {
    docker {
      image 'sonarsource/sonar-scanner-cli'
    }

  }
  stages {
    stage('Sonar Scanner') {
      steps {
        withSonarQubeEnv('Sonar') {
          waitForQualityGate true
        }

      }
    }

  }
}