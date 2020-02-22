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
  }
}
