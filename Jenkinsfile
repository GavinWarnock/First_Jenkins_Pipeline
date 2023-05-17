
pipeline {
  agent any
  
  stages {
    
    stage('Build') {
    
      steps {
        sh 'echo "Buidling the application..."'
      }
    }
     stage('Docker') {
       
        steps {
          withCredentials([usernamePassword(credentialsId: 'personal-docker-credentials', userNameVariable: 'DOCKER_USERNAME', passwordVariable: 'DOCKER_PASSWORD')]) {
            sh "echo ${DOCKER_USERNAME}" 
          }
      }
    }  
  }   
}
