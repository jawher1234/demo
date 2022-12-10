pipeline {
    agent {label "maven"}
 
    stages {

        stage('Git Checkout'){
            steps {
               git branch: 'main', url: 'https://github.com/jawher1234/demo.git'
            }
        }
            
        stage('version'){
            steps {
               
                sh "mvn --version"
                
            }
        }

        }

  }