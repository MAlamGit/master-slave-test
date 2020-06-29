pipeline {
	agent none

    stages {

		stage('ss-prod-master Jenkinsfile executing started') {
            agent { label 'ss-prod-master' }
           
		   load 'ss-prod-master/Jenkinsfile'
        }
		
		
		stage('fdc-jenkins Jenkinsfile executing started') {
            agent { label 'fdc-jenkins' }
				load 'fdc-jenkins/Jenkinsfile'
        }

    }

    post {
        success {
            echo 'This will run only if successful'
        }
    }
}