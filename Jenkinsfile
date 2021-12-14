pipeline {
   agent any
   tools {
     maven 'M2_HOME'
     jdk 'JAVA_HOME'
        } 
   stages {
     stage('Checkout from scm') {
        steps {
           git branch:'development', url: 'https://github.com/saran-devops/addressbook.git'
              }
            }
     stage('Code compile') {
         steps {
            sh 'mvn compile'
               }
              }
     stage('run unit test') {
         steps {
           sh 'mvn test'
               }
             }
stage('create package') {
     steps {
       sh 'mvn package'
           }
         }  
    }
 }       
