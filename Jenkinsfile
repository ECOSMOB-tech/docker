#!groovy_script
node{
  stage('checkout code'){
    git url:'https://github.com/ECOSMOB-tech/compose.git',branch:'main'
  }
  stage('connect to the dev server'){
   sshagent(['ubun']) {
            sh 'scp -o StrictHostKeyChecking=no  docker-compose.yml ubuntu@3.109.121.141:'
            sh 'ssh -o StrictHostKeyChecking=no ubuntu@3.109.121.141 sudo docker-compose up -d'
            }
          }
}
  
