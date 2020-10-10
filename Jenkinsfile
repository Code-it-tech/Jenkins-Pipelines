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
   
   parameters {

      string(name:'app_name', defaultValue: "newapp")
      string(name:'account_name', defaultValue: "newapp2")
      choice(name:'region', choices: ['us-east-1', 'us-east-2', 'us-east-3'])
      
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
              echo  "Name of the App is ${params.app_name} and ${params.app_name2} "
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