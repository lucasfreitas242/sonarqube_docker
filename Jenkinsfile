pipeline {
    agent { docker { image 'sonarsource/sonar-scanner-cli' } }
    stages {
        stage('build') {
            steps {
                sh 'hello world'
            }
        }
    }
}