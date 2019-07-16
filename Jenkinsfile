#!/usr/bin/env groovy

/**
@Author 
Galam Sivakrishna
**/

node {
   def mvnHome
   stage('SCM Checkout') { // for display purposes
      // Get some code from a GitHub repository
             git'https://github.com/galamsiva2020/Javaweb.git'

   }
  
stage('Maven Build') {
      // Run the maven build
	  
    mvnHome ='D:/GALAM/SivaDevopsSoftwares/apache-maven-3.6.0-bin/apache-maven-3.6.0'
    
//withEnv(["MVN_HOME=C:/Users/raju_/Downloads/apache-maven-3.6.1"]) {
         //if (isUnix()) {
//sh '"$MVN_HOME/bin/mvn" -Dmaven.test.failure.ignore clean package'
  //       } else {
    //        bat(/"%MVN_HOME%\bin\mvn" -Dmaven.test.failure.ignore clean package/)
      //   }
      //}
   }
   
stage('TestResults') {
      junit '**/target/surefire-reports/TEST-*.xml'
      archiveArtifacts 'target/*.jar'
   }
}

