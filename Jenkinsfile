pipeline{
  agent any
  tools {
    maven 'Maven' 
  }
 environment {
    ANYPOINT = credentials('ANYPOINT')
 }
 stages {
 	stage ('Build'){
 		steps {
		
 				bat 'mvn clean install'
 			
 		}
 	}
 	stage ('Deploy'){
 		steps {
 				bat 'mvn  package deploy  -Dusername=MSIMULE -Dpassword=MSImule@1 -Denvironment=Sandbox -DmuleDeploy'
 			
 		}
 	}
 }

}
