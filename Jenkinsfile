pipeline {
	agent any

    stages {

		stage('ss-prod-master) {
            agent { label 'ss-prod-master' }
            steps {
                sh '''	echo  "ss-prod-master Jenkinsfile executing started....."  '''
				
				load 'ss-prod-master/Jenkinsfile'
            }
        }
		
		
		stage('fdc-jenkins') {
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