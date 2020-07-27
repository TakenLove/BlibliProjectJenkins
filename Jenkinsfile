pipeline {
 agent {
   label 'docker-vm'
 }
 
 stages {
   stage ('Test Pipeline') {
     steps {
      echo "Show Docker"
      echo "Start Docker"
      sh '''
        docker --version
        docker image ls
        docker container ls
        
        echo "You can do docker-compose, adn other command her!!"
      '''
     }
   }
 
 }
}
