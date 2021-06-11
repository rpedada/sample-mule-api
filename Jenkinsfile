pipeline {

agent any

stages{

	stage("Build") {
	steps {
	
	bat 'mvn clean install'
	}
	}
	
	stage("Test") {
	steps {
		echo "testing application"
	}
	
}
	
	stage ("Deploy") {
	steps {
		echo "Deploy application successfully"
		}
		
	}
	}
		}
