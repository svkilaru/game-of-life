pipeline {
    agent any
  
   

    stages {
        stage('Configure') {     
            env.PATH = "${tool 'maven-3.5.2'}/bin:${env.PATH}"   
        }
        stage('Build') { 
            steps { 
                
                sh "mvn clean compile" 
            }
        }
        stage('Test'){
            steps {
                  
                  sh "mvn test" 
                
            }
        }
        stage('Deploy') {
            steps {
                  
                  sh "mvn deploy"
                
            }
        }
    }
}
