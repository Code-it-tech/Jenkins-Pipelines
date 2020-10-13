

pipeline {

   agent none
   options {
      timestamps()
           } 
   
    stages {
        stage('Docker Front-End') {
        agent {
        docker  { image 'node:14-alpine' }
              }  
        options {
         timeout(time:40 , unit:'SECONDS')
              }
        input {
                message "Should we continue?"
                ok "Yes, we should."  
            }
           steps {
                 sh "node --version"
               }
        }

        stage('Docker Back-End') {
        agent {
        docker  { image 'maven:3-alpine' }
              }  
        options {
         timeout(time:50 , unit:'SECONDS')
              }
        input {
                message "Should we continue?"
                ok "Yes, we should."  
            }
           steps {
                 sh "mvn --version"
               }
        }
    }
}