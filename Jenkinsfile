pipeline {
       agent {
        docker {
            image 'maven:3.3-jdk-8-alpine'
            args '-v /root/.m2:/root/.m2' && \
               ${PWD}:/usr/src/mymaven
            
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
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
