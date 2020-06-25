pipeline {
	agent { label env.Slave }

    stages {
        stage('stage-01') {
            
            steps {
                echo 'Building..'
                sh '''	echo  "stage-01 steps" 
				
				cd /opt/
				chmod +x /opt
				mkdir slave-build
				'''
            }
        }
		
		stage('stage-02') {
            
            steps {
                echo 'Testing..'
                sh '''	
				
				echo  "stage-02 steps " 
				cd /opt/
				chmod +x /opt
				mkdir slave-test
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