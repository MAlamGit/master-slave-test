
node {
    stage('Shared') {
        echo 'Shared stage'

        checkout scm
    }

    if (env.ENV == 'prod-slaves') {
        load 'prod-slaves/Jenkinsfile'
    } 
	
	else if (env.ENV == 'non-prod') {
        load 'non-prod/Jenkinsfile'
    }
}