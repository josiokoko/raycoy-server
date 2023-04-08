pipeline {
	agent any

	stages {
		stage("GitHub Checkout") {
			steps {
				echo "checking out of GitHub..."
			}
		}

		stage("Docker Build") {
			steps {
				echo 'Building docker image...'
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