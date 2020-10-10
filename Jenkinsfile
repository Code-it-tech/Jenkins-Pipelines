pipeline {

   environment {
     GREEN="\033[1;32m"
     RED="\033[1;31m"
     BLUE="\033[1;34m"
     Respect="Please Enter your"
     DIR="/opt"
     WORKSPACE_PATH="${env.WORKSPACE}"
   }

   agent any

   options {
      timestamps()
      ansiColor("xterm")

   } 

   stages {
    
    stage('Install Softwares') {
      options {
      timeout(time:20, unit: "SECONDS")

      }

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
          echo "${Respect}  username" 
         }
      }
    stage('Email') {
       steps {
          echo "${Respect}  username" 
       }
     }
   }
}