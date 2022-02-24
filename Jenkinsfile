pipeline {
    agent any
    stages {
        stage('Git') {
            steps{
                credentialsId: 'jenkins',
                git branch: 'master',
                url: 'https://github.com/lucasfreitas242/sonarqube_docker'
            }
        }
        stage('SonarQube') {
            steps{
                withSonarQubeEnv('sunarqube') {
                    sh 'mvn sonar:sonar -Dsonar.projectKey=codeedu-desafio   -Dsonar.sources=.   -Dsonar.host.url=http://localhost:9000   -Dsonar.login=9d7ab101ef8897356eb9ce55395bc4'
                }
            }
        }
    }
}