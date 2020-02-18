pipeline{
 agent any
 stages {
 	stage ('Build Application'){
 		steps {
 			
 				bat 'mvn clean install'
 		}
 	}
 	
 	stage ('Test Application'){
 		steps {
 			
 				bat 'mvn clean test'
 		}
 	}

 	stage ('Deploy Application'){
 		steps {
 			
 				bat 'mvn clean package deploy -Dmule.version=4.2.2 -Dusername=max356 -Dpassword=@@Gaga356@@ -Denvironment=Sandbox -Dworkers=1 -Dworker.type=Micro -Dapplication.name=Craft-greeting-API -DmuleDeploy'
 			}
 		}
 	}
 }