pipeline {
    agent any
 
    stages {

        stage('Git Checkout'){
            steps {
               git branch: 'main', url: 'https://github.com/jawher1234/demo.git'
            }
        }
            
        stage('version'){
            steps {

               def mvnHome = tool name: 'maven', type: 'maven'
               sh "${mvnHome}/bin/mvn package"
                
            }
        }

        }

  }