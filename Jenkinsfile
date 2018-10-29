#!/usr/bin/env groovy
node {  
    stage('Build') { 
       echo "Build Stage" 
       checkout scm
       deleteDir();
       mvnHome = tool 'M3'
       sh '${mvnHome}mvn clean package'
    }
    stage('Test') { 
        echo "Test Stage"  
        sh '${mvnHome}mvn test'
    }
    stage('Deploy') { 
        echo "Deploy Stage" 
    }
   }