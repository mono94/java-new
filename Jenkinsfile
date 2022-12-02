pipeline{
    agent any
    environment{
        
        registry = "sree819/my-repo"
        registryCredential = 'docker-hub'        
    }
    
    stages{
       stage('Building image') {
      steps{
       
          dockerImage = docker.build registry + ":$BUILD_NUMBER"
        
      }
    }
       stage('Deploy Image') {
      steps{
         
            docker.withRegistry( '', registryCredential ) {
            dockerImage.push()
         
        }
      }
    }

