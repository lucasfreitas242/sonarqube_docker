node("master") {         


		stage('SCM') {

			git branch: 'master', 
			credentialsId: 'jenkins', 
			url: 'https://github.com/lucasfreitas242/sonarqube_docker'
		}

		stage('Mvn Package'){

			sh 'mvn clean package'
		}

		stage('SonarQube analysis') {

			withSonarQubeEnv('sonarqube') {

				sh 'mvn sonar:sonar -Dsonar.projectKey=teste2 -Dsonar.host.url=http://localhost:9000 -Dsonar.login=f229f79b0129f7e3c2af63c9927807f18d0042a1'

			}

		}

}        
