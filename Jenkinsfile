pipeline {

   agent any 

   stages {
    
    stage('Install Docker') {
       when {
          branch 'Branch2'      
         }
       steps {
           sh "chmod +x docker.sh"
           sh "./docker.sh"
       }
    }
   }
  }
