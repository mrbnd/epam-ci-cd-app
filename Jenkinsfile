pipeline {
  agent {
    kubernetes {
      yamlFile 'agent.yaml'
    }
  }
  stages {
    stage('Docker Build') {
      steps {
	container('sonar') {
        	sh "sonar-scanner   -Dsonar.projectKey=epam-cicd   -Dsonar.sources=."
	}
      }
    }
}
}
