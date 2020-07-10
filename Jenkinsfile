
node {
    stage('Shared') {
        echo 'Shared stage'

        checkout scm
    }

    if (env.JOB_NAME == 'ss-prod-master') {
        load 'ss-prod-master/Jenkinsfile'
    } 
	else if (env.JOB_NAME == 'fdc-jenkins') {
        load 'fdc-jenkins/Jenkinsfile'
    }
}