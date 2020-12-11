pipeline {
    agent any
    parameters{
	    gitParameter branch: '', branchFilter: 'origin/(.*)', defaultValue: 'master', description: '', name: 'branch', quickFilterEnabled: true, selectedValue: 'DEFAULT', sortMode: 'DESCENDING_SMART', tagFilter: '*', type: 'PT_BRANCH', useRepository: 'ssh://git@github.com:ATolkachev/epam-ci-cd-app.git’
    }
	    
    stages {
        stage('Ls') {
            steps {
		    git branch: "${param.branch}", url: 'ssh://git@github.com:ATolkachev/epam-ci-cd-app.git', credentialsId: 'atolkachev'
            }
        }
	stage('git') {
            steps {
                sh git status'
            }
        }
    }
}
