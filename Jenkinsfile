pipeline {
  agent any

  stages {
      stage('test ssh remote execution') {
          steps {

             sshagent(['docker1-ubuntu']) {
                 // some block
                 sh "ssh -o StrictHostKeyChecking=no -l ubuntu <remote_ip> 'whoami'"
             }
         }
      }
   }
}