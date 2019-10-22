pipeline{
 agent any
 environment {
    ANYPOINT = credentials('ANYPOINT-LOCAL')
 }
 stages {
 	stage ('Build'){
 		steps {

 				sh '"$MVN_HOME/bin/mvn" clean compile'

 		}
 	}
 	
 }

}
