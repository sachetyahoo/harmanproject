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
            sh "packer build packer.json"  
          }
      }
  }
}
