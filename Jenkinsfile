pipeline {
       agent {docker
			{ image 'maven:latest'}
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
