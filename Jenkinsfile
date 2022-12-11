pipeline {
agent any
     
      tools {
    maven 'M3'
  }
     
     
         environment {
        registryCredential = 'dockerHub'
        registry = "faroukfarouk/tpachatproject:1.0"
    }

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
     
     
         post {
         always {
            junit(testResults: 'target/surefire-reports/*.xml', allowEmptyResults : true)
        }
         success {
            emailext attachLog: true, body: '''End of Pipeline
            Finished: SUCCESS''', subject: '#Success', to: 'jawher.zeiri@esprit.tn'
         }
         failure  {
            emailext attachLog: true, body: '''End of Pipeline
            Finished: FAILURE''', subject: '#Failure', to: 'jawher.zeiri@esprit.tn'
         }
     
    }
     
     
}
