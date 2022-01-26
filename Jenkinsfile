pipeline {
  agent any

  stages {
      stage('test ssh remote execution') {
          steps {

             sshagent(credentials:['docker2-ubuntu']) {
                 // some block
                 sh "ssh -o StrictHostKeyChecking=no -l ubuntu 172.31.92.245 'whoami'"
                 sh "ssh -o StrictHostKeyChecking=no -l ubuntu 172.31.92.245 'touch itworks.txt'"
             }
         }
      }
   }
}