pipeline{
    agent any
    stages{
      stage('Docker build image'){
        steps{
            bat 'docker build -t asa/jenkins-pipeline-docker-demo .'
            //sh 'docker build -t asa/jenkins-pipeline-docker-demo .'
        }
      }
    }
}
