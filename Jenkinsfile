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
 				bat 'mvn -f mule4cicd/pom.xml package deploy  -Dusername=$ANYPOINT_USR -Dpassword=$ANYPOINT_PSW -Denvironment=Sandbox -DmuleDeploy'
 			
 		}
 	}
 }

}
