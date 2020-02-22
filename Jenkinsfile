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
	sh 'docker build tesk-docker/ -t mywebhttpd:v4 --no-cache'
      }
    }
    stage('Running Docker Image') {
      steps {
        sh 'docker run -dit -p 80:80 -d mywebhttpd:v4'
      }
    }
    stage('Running Web server'){
      steps {
        sh 'echo "check your webpage"'
      }
    }
  }
}
