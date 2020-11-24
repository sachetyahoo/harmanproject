pipeline {
    agent any
  stages {
    stage('Deploy') {
            steps {
                sshagent(['harman_deploy']) {
            sh "scp -i /home/ubuntu/ncal.pem -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/Deploy/index.html  ubuntu@172.31.4.79:/var/www/html/"
            }
        }
       }
    }
}
