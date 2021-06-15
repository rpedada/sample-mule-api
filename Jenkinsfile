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
	
	stage ("Deploy to Development") {
  	environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint.credentials') 
      }	 
	 steps {
            bat 'mvn -U -V -e -B -DskipTests deploy -DmuleDeploy -Dmule.version="4.3.0" -Danypoint.username="%ANYPOINT_CREDENTIALS_USR%" -Danypoint.password="%ANYPOINT_CREDENTIALS_PSW%" -Dcloudhub.app="sample-mule-api-d" -Dcloudhub.environment="Sandbox" -Dcloudhub.bg="wipro" -Dcloudhub.worker="micro"'
      }
    }
		
	}
		}
