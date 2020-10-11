pipeline {

   agent any

   stages {
    
    stage('Install Docker') {
      steps {
          sh "chmod +x docker.sh"
          sh "./docker.sh"
    }
   }
  }
}