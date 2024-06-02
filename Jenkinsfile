pipeline{
    environment {
        registry = "demo/jenkins-pipeline-doker-demo"
        registryCredential = 'dockerhub_id'
        dockerImage = ''
    }
    agent any
    stages{
	
		stage('Checkout'){
			steps{
				git branch: 'main', url: 'https://github.com/asa-7670/jenkins-pipeline-docker-demo'
			}
		}
		stage('Docker build image'){
			steps{
				script {
					dockerImage = docker.build registry + ":$BUILD_NUMBER"
				}
			}
		}
		stage('Docker Push image'){
			steps{
				script {
					docker.withRegistry( '', registryCredential ) {
						dockerImage.push()
					}
				}
			}
		}
		stage('Cleaning up') {
			steps {
				sh 'docker rmi $registry:$BUILD_NUMBER'
			}
		}
	}
}
