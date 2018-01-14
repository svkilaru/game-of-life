pipeline {
    agent any
    def mvnHome = tool 'M2_HOME'
   

    stages {
        stage('Build') { 
            steps { 
                sh "${mvnHome}/bin/mvn clean compile" 
            }
        }
        stage('Test'){
            steps {
                
                  sh "${mvnHome}/bin/mvn test" 
                
            }
        }
        stage('Deploy') {
            steps {
                
                  sh "${mvnHome}/bin/mvn deploy"
                
            }
        }
    }
}
