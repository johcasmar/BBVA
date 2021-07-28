pipeline {
    agent {
         docker { image 'oracle_mvn:latest' }
              }
             environment {
                WORKSPACE = "${WORKSPACE}" 
                }
    stages {
        stage('Checkout - Build') {
            steps {
                sh ('mvn package  -DoracleHome=/u01/oracle/ -Dversion=12.2.1-0-0 ' )
                 echo 'Construccion componente OSB..'
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
