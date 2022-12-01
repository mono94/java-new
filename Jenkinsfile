pipeline {
  agent any
  stages {
    stage('Build image') {
      steps {
        echo ("hello world")
		script {
                      docker build -t "my-qbc" .
		}
        } 
       }
    }
  }
