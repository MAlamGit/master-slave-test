
node {
    stage('Shared') {
        echo 'Shared stage'

        checkout scm
    }

    if (env.JOB_NAME == 'prod-slaves') {
        load 'prod-slaves/Jenkinsfile'
    } 
	
	else if (env.JOB_NAME == 'non-prod') {
        load 'non-prod/Jenkinsfile'
    }
}