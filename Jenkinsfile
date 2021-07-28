pipeline {
       agent any
    stages {
        stage('Build') {
            steps {
                sh 'docker run --rm -v /root/.m2:/root/.m2 -v $PWD/java-app:/app -w /app maven:3-alpine mvn -B -DskipTests clean package'
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
