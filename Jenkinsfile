pipeline {

   agent {
       docker  { image 'node:14-alpine' }
   }
   options {
      timestamps()
           } 
   
    stages {
        stage('Docker') {
        options {
         timeout(time:20 , unit:'SECONDS')
              }
        input {
                message "Should we continue?"
                ok "Yes, we should."
                
            }
           steps {
                 sh 'cd /var/run'
                 sh 'chmod 666 /var/run/docker.sock'
                 sh 'sudo node --version'r
               }
        }
    }
}