environment {
        gitBranch = scm.branches[0].toString().replace('*/','')
}

pipeline {
    agent any
    
    stages {
        stage('Ls') {
            steps {
                sh 'ls'
            }
        }
	stage('Ls -la') {
            steps {
                sh 'ls -la'
            }
        }
	    stage('env'){
		    steps {
			    script {
				    echo "${env.gitBranch}"
			    }
		    }
	    }
    }
}
