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
                
               def mvnHome = tool name: 'maven 3.6.3', type: 'maven'
               sh "${mvnHome}/bin/mvn -B -DskipTests clean package"
                
            }
        }

        }

  }