pipeline{
 agent any
 environment {
    ANYPOINT = credentials('ANYPOINT-LOCAL')
 }
 stages {
 	stage ('Build'){
 		steps {
 			
 				bat 'mvn clean compile'
 			
 		}
 	}
 	stage ('Deploy'){
 		steps {
 			withMaven(maven:'maven'){
 				sh 'mvn -f mule-jenkins-pipeline/pom.xml package deploy  -Dusername=$ANYPOINT-LOCAL_USR -Dpassword=$ANYPOINT-LOCAL_PSW -Denvironment=Development -DmuleDeploy'
 			}
 		}
 	}
 }

}
