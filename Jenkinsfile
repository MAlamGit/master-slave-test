pipeline {
agent any
     stages {
        stage ('Main Stage') {
            steps {
                script {
                    if (env.SS_PROD_FDC_PIPELINE equals(ss-prod-master)){
                        stage ('ss-prod-master Jenkinsfile executing started') {
                            sh 'ss-prod-master Jenkinsfile executing started......'
							String jenkinsFile_ssProdMaster = /ss-prod-master/Jenkinsfile
							load jenkinsFile_ssProdMaster
                        }
                    }
					
                    if (env.SS_PROD_FDC_PIPELINE equals(fdc-jenkins)) {
                        stage ('fdc-jenkins Jenkinsfile executing started') {
                            sh 'fdc-jenkins Jenkinsfile executing started......'
							String jenkinsFile_ssProdMaster = /ss-prod-master/Jenkinsfile
							load jenkinsFile_fdcJenkins
                        }
                    }
                }
            }
        }
    }
}
