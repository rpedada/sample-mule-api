pipeline {

agent any

stages{

	stage("Build") {
	steps {
	
	sh 'mvn clean package'
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
		}
