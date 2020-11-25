pipeline {
    agent any
  stages {
      stage ('Clone') {
          steps {
              sh "git pull origin main"
          }
      }
      stage('Packer Image') {
          steps {
            sh "sudo packer build packer.json"  
          }
      }
  }
}
