pipeline {
	agent n

    stages {

		stage('ss-prod-master Jenkinsfile executing started') {
            agent { label 'ss-prod-master' }
            steps {
                sh '''	echo  "ss-prod-master Jenkinsfile executing started....."  '''
				
				load 'ss-prod-master/Jenkinsfile'
            }
        }
		
		
		stage('fdc-jenkins Jenkinsfile executing started') {
            agent { label 'fdc-jenkins' }
            steps {
                sh ''' echo  "fdc-jenkins Jenkinsfile executing started......"  '''
				
				load 'fdc-jenkins/Jenkinsfile'
            }
        }

    }

    post {
        success {
            echo 'This will run only if successful'
        }
    }
}