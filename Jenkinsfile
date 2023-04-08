pipeline {
	agent any

	environment {
		DOCKERHUB_CREDENTIALS=credentials('josiokoko')
	}

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
				sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
				echo 'Login complete...'
			}
		}

		stage("Push") {
			steps {
				echo 'pushing ...'
			}
		}

		stage("Logout") {
			steps{
				sh 'docker logout'
				echo 'Logout successful!'
			}
		}

	}

}