pipeline{
    agent any
    stages{
     stage('Checkout'){
         checkout scmGit(branches: [[name: '*/main']], 
                         extensions: [], 
                         userRemoteConfigs: [[url: 'https://github.com/asa-7670/jenkins-pipeline-docker-demo']])
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
