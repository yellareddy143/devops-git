pipeline {
  agent jenkins-node1
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
	sh 'docker build tesk-docker/ -t devops-repo:latest '
      }
    }
    stage('PUSH TO ECR') {
      steps {
        sh '$(aws ecr get-login --no-include-email --region ap-south-1)'
	sh 'docker tag devops-repo:latest 514224277819.dkr.ecr.ap-south-1.amazonaws.com/devops-repo:latest'
	sh 'docker push 514224277819.dkr.ecr.ap-south-1.amazonaws.com/devops-repo:latest'
      }
    }
    stage('Check Your AWS ECR'){
      steps {
        sh 'echo "DOCKER IMAGE PUSHED SUCCESSFULLY"'
      }
    }
  }
}
