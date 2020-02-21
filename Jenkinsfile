
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
        }
        }

        stage ('bulid docker image') {
                steps {
                sh 'echo "buliding docker image"'
		sh 'docker build /tesk-docker/ -t webserver:v1'
                }
        }
}
}
