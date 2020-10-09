pipeline {

   environment {
     GREEN="\033[1;32m"
     RED="\033[1;31m"
     BLUE="\033[1;34m"
     Respect=""
     DIR="/opt"
   }

   agent any 

   stages {
    
    stage('Install Softwares') {
      steps {
          echo "Installing Softwares ....."
          
          dir ("${DIR}") {
           
              sh "sudo apt update"
              sh "sudo apt install maven"
              sh "mvn -version"
              sh "sudo apt install default-jdk"
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