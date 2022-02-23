pipeline {
    agent { docker { image 'sonarqube:8.9.7-community' } }
    stages {
        stage('build') {
            steps {
                sh 'node --version'
            }
        }
    }
}