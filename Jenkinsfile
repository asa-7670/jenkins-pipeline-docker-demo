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
            script {
                sh 'docker build -t demo/jenkins-pipeline-docker-demo .'
            }
        }
      }
      stage('Docker Push image'){
        steps{
            script {
                //sh 'docker push -t demo/jenkins-pipeline-docker-demo .'
                echo 'push  to docket hub'
            }
        }
      }
    }
}
