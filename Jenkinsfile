pipeline {
	agent { label env.Slave }

    stages {
        stage('stage-01') {
            
            steps {
                echo 'Building..'
                sh '''	echo  "stage-01 steps" 
				
				cd /opt/alam-workspace
				chmod 777 test.sh
				./test.sh
				'''
            }
        }
		
		stage('stage-02') {
            
            steps {
                echo 'Testing..'
                sh '''	
				
				echo  "stage-02 steps " 
				cd /opt/alam-workspace
				chmod 777 test.sh
				./test.sh
				
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