pipeline {
    agent any
 
    stages {

        stage('Git Checkout'){
            steps {
               git branch: 'main', url: 'https://github.com/jawher1234/demo.git'
            }
        }
            
        stage('Maven version'){
            steps {
                sh "mvn clean package"
            }

        }

  }
}