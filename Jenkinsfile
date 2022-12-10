pipeline {
    agent any


        environment {
           PATH = "/usr/bin/mvn:$PATH"
    }
 
    stages {

        stage('Git Checkout'){
            steps {
               git branch: 'main', url: 'https://github.com/jawher1234/demo.git'
            }
        }
            
        stage('maven'){
            steps {

               sh "mvn test"
                
            }
        }

        }

  }