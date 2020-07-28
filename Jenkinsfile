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
       docker-compose up -f docker-compose.yml $(cat arguments/compose-arguments)
      '''
     }
   } 

   stage ('Deploy: Show Docker Compose Result') {
     steps {
       sh '''
        cd Docker
        docker-compose -f docker-compose.yml ps
        docker-compose container ls 
       '''
     }
   }

 }
}
