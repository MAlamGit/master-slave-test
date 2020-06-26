pipeline {
	agent { label 'master'}

    stages {
        stage('stage-01') {
            agent { label env.FDC_SLAVE01 }
            steps {
                echo 'Building..'
                sh '''	echo  "stage-01 steps" 
				
				cd /opt/alam-workspace
				chmod u+x test.sh
				./test.sh
				'''
            }
        }
		
		stage('stage-02') {
            agent { label env.FDC_SLAVE02 }
            steps {
                echo 'Testing..'
                sh '''	
				
				echo  "stage-02 steps " 
				cd /opt/alam-workspace
				 chmod u+x test.sh
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