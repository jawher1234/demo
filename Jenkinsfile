pipeline {
agent any

     stages {
          
       stage('Build') {
           steps {
             sh "mvn install"
                 //sh "mvn compile"
            }
        }
            
        stage('Maven version'){
            steps {
                sh "mvn -version"
            }

        }

  }
}
