pipeline {
 agent {
   label 'docker-vm'
 }
 
 stages {
   stage ('Test Pipeline') {
     steps {
      echo "Show Docker"
      sh '''
        docker --version
        docker image ls
        docker container ls
        
        echo "You can do docker-compose, adn other command her!!"
      '''
     }
   }
   
   stage ('Deployment : Docker Compose And Load Balancer') {
     steps {
      sh '''
       cd Docker
       docker-compose up -f docker-compose.yml $(cat docker/compose-arguments)

      '''
     }
   } 
 }
}
