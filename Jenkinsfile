pipeline {
    agent any
    parameters{
	     string( defaultValue: '', name: 'branch', description: 'Branch')
    }
	    
    stages {
        stage('Ls') {
            steps {
		    git branch: "${env.branch}", url: 'ssh://git@github.com:ATolkachev/epam-ci-cd-app.git', credentialsId: 'atolkachev'
            }
        }
	stage('git') {
            steps {
                sh 'git status'
            }
        }
    }
}
