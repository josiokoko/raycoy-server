pipeline {
	agent any

	stages {
		stage("GitHub Checkout") {
			steps {
				git branch: 'main', url: 'https://github.com/josiokoko/raycoy-server.git'
			}
		}

		stage("Docker Build") {
			steps {
				sh 'docker image build -t josiokoko/raycoy-things .'
			}
		}

		stage("Authenticate to DockerHub") {
			steps {
				echo 'Authenticating...'
			}
		}

		stage("Push") {
			steps {
				echo 'Pushing image to dockerhub...'
			}
		}

	}

}