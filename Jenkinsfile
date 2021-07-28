pipeline {
     agent {
            agent {docker{ image 'node:latest'}
				}
    stages {
        stage('Build') {
            steps {
                sh 'mvn --version'
            }
        }
       /* stage('Test') {
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
