pipeline {

   environment {
     GREEN="\033[1;32m"
     RED="\033[1;31m"
     BLUE="\033[1;34m"
     DIR="/opt"
     WORKSPACE_PATH="${env.WORKSPACE}"
     
     
   }

   agent any

   options {
      timestamps()
     } 
   
   parameters  {
 
         string(name:'app_name', value: "newapp")
   }

   stages {
    
    stage('Install Softwares') {
      options {
      timeout(time:20, unit: "SECONDS")

      }

      steps {
          echo "Installing Softwares ....."
          
          dir ("Softwares") {
              
              echo  "${env.WORKSPACE}" 
              echo  "Name of the App is ${params.app_name} "
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
          echo "${env.BUILD_TAG}  username" 
         }
      }
    stage('Email') {
       steps {
          echo "${BUILD_TAG}  username" 
       }
     }
   }
}