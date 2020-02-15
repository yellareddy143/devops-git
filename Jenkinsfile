
pipeline {
  agent any
   tools {
   maven "mvn"
   jdk   "jdk"
   }

   stages {
        stage ('git clone and build') {
        steps {
        sh 'echo "script started for bulinding code"'
        sh 'mvn clean'
        sh 'mvn install'
        }
        }

        stage ('bulid docker image') {
                steps {
                sh 'echo "buliding docker image"'
                }
        }
}
}
