
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
		sh 'docker build tesk-docker/ -t webserver:v1'
                }
        }
	stage ('Running docker Container') {
                steps {
                sh 'echo "Running docker"'
                sh 'docker run –dit –p 1234:80 webserver:v1'
                }
        }
	stage ('check the your container website'){
	steps {
	  sh ' echo "check the besite using your public IP"'
	  }
	  }
}
}
