pipeline {
  agent {
    docker {
      image 'sonarqube'
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