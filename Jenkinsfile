pipeline {
         agent {
             docker {
                 image 'maven:latest'
                 args '-v /root/.m2:/root/.m2'
             }
		}
    stages {
        stage('Build') {
            steps {
               sh ('''
					 echo ********************
					 echo *Build*
					 echo ********************
					 mvn -B -DskipTests clean package
				''')
            }
        }
        stage('Test') {
            steps {
               sh ('''
					 echo ********************
					 echo *Desplegando el jar*
				     echo ********************
					 mvn test
				''')
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
      /*  stage('Deliver') {
            steps {
                sh './jenkins/scripts/deliver.sh'
            }
        }*/
    }
}
