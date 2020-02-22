pipeline {
  agent any
  stages {
    stage('build') {
      steps {
      	sh 'echo "first pipe"'
      }
    }
    stage('clone') {
      steps {
        sh 'echo "stage started"'
	sh 'echo "stage 2 ended"'
      }
    }
    stage('Buliding docker image') {
      steps {
        sh 'echo "buliding docker image"'
	sh 'docker bulid --tag webserver:v1 tesk-docker/'
      }
    }
    stage('Running Docker Image') {
      steps {
        sh 'docker run --port 80:80 -d webserver:v1'
      }
    }
    stage('Running Web server'){
      steps {
        sh 'echo "check your webpage"'
      }
    }
  }
}
