pipeline {

   environment {
     GREEN="\033[1;32m"
     RED="\033[1;31m"
     BLUE="\033[1;34m"
     Respect=""
     DIR="/opt"
     WORKSPACE_PATH="${env.WORKSPACE}"
   }

   agent any 

   stages {
    
    stage('Install Softwares') {
      steps {
          echo "Installing Softwares ....."
          
          dir ("Softwares") {
           
              sh "sudo apt-get -y update"
              sh "sudo apt-get -y install maven"
              sh "mvn -version"
              sh "sudo apt-get -y install default-jdk"
              sh "java -version"

          }     
       }
   }
    stage('password') {
       steps {
          echo "${Respect} Please Enter your username" 
         }
      }
    stage('Email') {
       steps {
          echo "${Respect} Please Enter your username" 
       }
     }
   }
}