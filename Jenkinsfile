pipeline {
    agent any
    tools { 
        maven 'maven 3.6.3'  
    }

    stages {

                stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
            }
        } 

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