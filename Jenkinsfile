pipeline{
    agent any
    stages{
      stage('Docker build image'){
        steps{
            bat 'docker build -t demo/jenkins-pipeline-docker-demo .'
            //sh 'docker build -t demo/jenkins-pipeline-docker-demo .'
        }
      }
      stage('Docker Push image'){
        steps{
            bat 'docker push -t demo/jenkins-pipeline-docker-demo .'
            //sh 'docker push -t demo/jenkins-pipeline-docker-demo .'
        }
      }
    }
}
