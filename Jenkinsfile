pipeline{
    agent any
    stages{
     stage('Checkout'){
        steps{
          git branch: 'main', url: 'https://github.com/asa-7670/jenkins-pipeline-docker-demo'
        }
     }
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
