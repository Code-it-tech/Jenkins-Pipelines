pipeline {

   environment {
   
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
      string(name:'account_name', defaultValue: "1234567890")
      string(name:'aws_service', defaultValue: "Elasticbeanstalks")
      choice(name:'aws_region', choices: ['us-east-1', 'us-east-2', 'us-east-3'])
      
              }  

   stages {
    
    stage('Information') {
      options {
         timeout(time:20 , unit:'SECONDS')
              }
       input {
                message "Should we continue?"
                ok "Yes, we should."
                
            }
         steps {
          echo  "I am Performing Tasks on ${env.BRANCH_NAME} and in ${params.account_name} Account in ${params.aws_region} Region" 
          echo  "Name of the App is ${params.app_name}"
               }
    }
    stage('Install Softwares') {
      options {
        timeout(time:20, unit: "SECONDS")
              }

      steps {
          echo "Installing Softwares..."
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
       options {
         timeout(time:20 , unit:'SECONDS')
               }
       steps {
          echo "${env.BUILD_TAG}  username" 
             }
     }
   
     }
   }
