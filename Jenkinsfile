pipeline {
  agent any
  stages {
    stage('build') {
      step`s {
      	sh 'echo "first pipe"'
      }
    }
    stage('clone'){
      steps {
        sh 'echo "stage started"'
	sh 'stage 2 ended"'
      }
    }
  }
}
