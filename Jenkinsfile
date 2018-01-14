pipeline {
    agent any 

    stages {
        stage('Build') { 
            steps { 
                withMaven (maven : 'M2_HOME') {
                  sh 'mvn clean compile' 
                }
            }
        }
        stage('Test'){
            steps {
                withMaven (maven : 'M2_HOME') {
                  sh 'mvn test' 
                }
            }
        }
        stage('Deploy') {
            steps {
                withMaven (maven : 'M2_HOME') {
                  sh 'mvn deploy' 
                }
            }
        }
    }
}
