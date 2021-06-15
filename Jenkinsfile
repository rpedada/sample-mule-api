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
	when {
                branch 'dev'
         }
		 
	 steps {
            bat 'mvn -U -V -e -B -DskipTests deploy -DmuleDeploy -Dmule.version="4.3.0" -Danypoint.username="rpedada_june21" -Danypoint.password="Rpedada@1" -Dcloudhub.app="sample-mule-api-d" -Dcloudhub.environment="Sandbox" -Dcloudhub.bg="wipro" -Dcloudhub.worker="1"'
      }
    }
		
	}
		}
