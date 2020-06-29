pipeline {
	agent any

    stages {
        if (env.SS_PROD_FDC_PIPELINE == 'ss-prod-master'){
		stage('ss-prod-master Jenkinsfile executing started') {
            agent { label 'ss-prod-master' }
            steps {
                sh '''	echo  "ss-prod-master Jenkinsfile executing started....."  '''
				
				load 'ss-prod-master/Jenkinsfile'
            }
        }
		}
		
		if (env.SS_PROD_FDC_PIPELINE == 'fdc-jenkins'){
		stage('fdc-jenkins Jenkinsfile executing started') {
            agent { label 'fdc-jenkins' }
            steps {
                sh '''	
				echo  "fdc-jenkins Jenkinsfile executing started......"  '''
				
				String jenkinsFile_ssProdMaster = fdc-jenkins/Jenkinsfile
				load 'jenkinsFile_fdcJenkins'
            }
        }
		}
    }

    post {
        success {
            echo 'This will run only if successful'
        }
    }
}