pipeline{
    agent any
    stages{
      stage('Docker build image'){
        steps{
          sh 'docker build -t asa/jenkins-pipeline-docker-demo .'
        }
      }
    }
}
