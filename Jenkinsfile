pipeline {
  agent any
  stages {
    stage('build') {
      stepes {
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
