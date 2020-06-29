pipeline {
	
agent any


	stage("ss-prod-master Jenkinsfile executing started") {
      String jenkinsFile_ssProdMaster = /ss-prod-master/Jenkinsfile
   }
   
   stage("fdc-jenkins Jenkinsfile executing started") {
      String jenkinsFile_fdcJenkins = /fdc-jenkins/Jenkinsfile
   }
   
   load jenkinsFile_ssProdMaster
   load jenkinsFile_fdcJenkins
}