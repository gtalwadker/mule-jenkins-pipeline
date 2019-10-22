pipeline{
 agent any
 environment {
    ANYPOINT = credentials('ANYPOINT-LOCAL')
 }
 stages {
 	stage ('Build'){
 		steps {

 				sh '/Users/gtalwadker/MuleSoft/apache-maven-3.6.0/bin/mvn clean package'

 		}
 	}


  stage ('Deploy'){
 		steps {

 				sh '/Users/gtalwadker/MuleSoft/apache-maven-3.6.0/bin/mvn package deploy -Dusername=$ANYPOINT-LOCAL_USR -Dpassword=$ANYPOINT-LOCAL_PSW -Denvironment=Development -DmuleDeploy'

 		}
 	}
 }

}
