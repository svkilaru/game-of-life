pipeline {
    agent any
  
   

    stages {
        stage('Build') { 
            steps { 
                def mvnHome = tool 'M2_HOME'
                sh "${mvnHome}/bin/mvn clean compile" 
            }
        }
        stage('Test'){
            steps {
                  def mvnHome = tool 'M2_HOME'
                  sh "${mvnHome}/bin/mvn test" 
                
            }
        }
        stage('Deploy') {
            steps {
                  def mvnHome = tool 'M2_HOME'
                  sh "${mvnHome}/bin/mvn deploy"
                
            }
        }
    }
}
