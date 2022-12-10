pipeline {
    agent any
    tools { 
        maven 'Maven 3.6.3' 
        jdk 'jdk8' 
    }
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
            }
        } 
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