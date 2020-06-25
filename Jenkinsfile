pipeline {
	agent { label '${Slave}​' }

    stages {
        stage('stage-01') {
            
            steps {
                echo 'Building..'
                sh '''	echo  stage-01 steps  
				
				cd opt/
				mkdir aster-slave-build
				'''
            }
        }
		
		stage('stage-02') {
            
            steps {
                echo 'Testing..'
                sh '''	
				
				echo  stage-02 steps  
				cd opt/
				mkdir master-slave-test
				'''
            }
        }
    }

    post {
        success {
            echo 'This will run only if successful'
        }
    }
}