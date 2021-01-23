pipeline {
  agent {
    docker {
      args "-v /var/run/docker.sock:/var/run/docker.sock"
      image "sonarsource/sonar-scanner-cli:4.5"
    }
  }
  stages {
    stage('ls') {
      steps {
	 sh "ls -la"
	
      }
    }
}
}
