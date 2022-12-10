pipeline {
    agent {label "agent"}
 
    stages {

        stage('Maven version'){
            steps {
               git branch: 'main', url: 'https://github.com/jawher1234/demo.git'
            }

        stage('Maven version'){
            steps {
                sh "mvn -version"
            }
        }

    }
  
}
