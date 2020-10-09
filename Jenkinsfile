pipeline {

   environment {
     GREEN="\033[1;32m"
     RED="\033[1;31m"
     BLUE="\033[1;34m"
   }

   agent any 

   stages {
    
    stage('username') {
     steps {
      sh " echo -e "${GREEN} Please Enter your username " "
    }
    }
    stage('password') {
     steps {
      sh " echo -e "${RED} Please Enter your password " "
         }
       }
    stage('Email') {
     steps {
      sh " echo -e "${BLUE} Please Enter your Email address " "
       }
     }
   }

}