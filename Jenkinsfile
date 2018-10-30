#!/usr/bin/env groovy
node {  
	agent {
	        docker {
	            image 'maven:3-alpine'
	            args '-v /root/.m2:/root/.m2'
	        }
	}
    stage('Build') { 
       echo "Build Stage" 
       checkout scm
       deleteDir();
       //mvnHome = tool 'M3'
       sh 'mvn clean package'
    }
    stage('Test') { 
        echo "Test Stage"  
        sh 'mvn test'
    }
    stage('Deploy') { 
        echo "Deploy Stage" 
    }
   }