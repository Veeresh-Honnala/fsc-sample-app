#!/usr/bin/env groovy
node {  
    stage('Build') { 
       echo "Build Stage" 
       checkout scm
       deleteDir();
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