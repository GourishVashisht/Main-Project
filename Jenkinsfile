pipeline {
    agent any
	
	triggers {
		pollSCM("H/2 * * * *")
	}
	
	parameters {
		string(name: "STRING", defaultValue: "String Value", description: "What is the string value ?")
		string(name: "NAME", defaultValue: "Gourish", description: "What is your name ?")
	}
	
    stages {
		stage('Project One'){
			steps{
				echo "${STRING_VALUE}"
				build job: 'project one',
				parameters: [
					[$class: 'StringParameterValue', name: 'STRING_VALUE', value: "${STRING}"]
				]
			}
		}
		stage('Project Two'){
			steps{
				echo "${NAME}"
				build job: 'project two',
				parameters: [
					[$class: 'StringParameterValue', name: 'MY_NAME', value: "${NAME}"]
				]
			} 
		}
	}
}
