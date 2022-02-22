pipeline {
  agent any
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