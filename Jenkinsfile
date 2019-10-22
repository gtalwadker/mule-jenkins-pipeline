pipeline{
 agent any
 environment {
    ANYPOINT = credentials('ANYPOINT-LOCAL')
 }
 stages {
 	stage ('Build'){
 		steps {
 			
 				sh 'mvn clean compile'
 			
 		}
 	}
 	stage ('Deploy'){
 		steps { 				sh 'mvn package deploy  -Dusername=$ANYPOINT-LOCAL_USR -Dpassword=$ANYPOINT-LOCAL_PSW -Denvironment=Development -DmuleDeploy'
 			
 		}
 	}
 }

}
