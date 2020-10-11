pipeline {

   agent {
      docker {image 'node:14-alpine'}      
   }

   stages {
    
    stage('test') {
      steps {
          sh "apt-get update"
          curl -fsSL "https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -"
          sh "apt-get install apt-transport-https ca-certificates curl software-properties-common"
          sh "add-apt-repository deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
          sh "node --version"
    }
   }
  }
}