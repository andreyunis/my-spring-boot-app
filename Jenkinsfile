pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Clona el repositorio
                git branch: 'main', url: 'https://github.com/andreyunis/my-spring-boot-app.git'
            }
        }
        stage('Build') {
            steps {
                // Construye el proyecto Maven
                bat 'mvn clean package'
            }
        }
	stage('Cleanup'){
		steps{
			//Limpieza despues de cada build
			cleanWs()
		}
	}
    }

}

