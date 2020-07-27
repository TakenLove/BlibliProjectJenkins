pipeline {
 agent {
   label 'docker-vm'
 }
 
 stages {
   stages ('Test Pipeline') {
     steps {
      echo "Show Docker"
      sh '''
        docker --version
        docker image ls
        
        echo "You can do docker-compose, adn other command her!!"
      '''
     }
   }
 
 }
}
