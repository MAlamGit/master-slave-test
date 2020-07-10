
node {
    stage('Shared') {
        echo 'Shared stage'

        checkout scm
    }

    if (env.JOB_NAME == 'ss-prod-master') {
        load 'prod-slaves/Jenkinsfile'
    } 
	else if (env.JOB_NAME == 'fdc-jenkins') {
        load 'non-prod/Jenkinsfile'
    }
}