pipeline {
    agent {	
		any
	}
	
    stages {
		stage('Project One'){
			steps{
				build job: 'project-one'
			}
		}
		stage('Project Two'){
			steps{
				build job: 'project-two'
			} 
		}
		stage('Project Three'){
			steps{
				build job: 'project three'
			} 
		}
	}
}
