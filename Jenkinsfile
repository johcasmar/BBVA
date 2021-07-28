pipeline {
       agent {
        docker {
            image 'maven:3.3-jdk-8-alpine'
                    
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn package'
            }
        }
        /*stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }*/
      }
    } 
