pipeline {
    agent any
  stages {
      stage ('Clone') {
          steps {
              sh "git pull origin main"
          }
      }
    stage('Deploy') {
            steps {
                sshagent(['harman_deploy']) {
            sh "scp -i /home/ubuntu/ncal.pem -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/Deploy-Pipeline/index.html  ubuntu@${Server_Ip}:/var/www/html/"
            }
        }
       }
    }
}
