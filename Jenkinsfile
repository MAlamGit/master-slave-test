pipeline {
    agent { label '${Slave}​' }

    stages {
        stage('stage-01') {
            
            steps {
                echo 'Building..'
                sh '''	echo  stage-01 steps  '''
            }
        }
		
		stage('stage-02') {
            
            steps {
                echo 'Building..'
                sh '''	echo  stage-02 steps  '''
            }
        }
    }

    post {
        success {
            echo 'This will run only if successful'
        }
    }
}