pipeline {
         agent {
             docker {
                 image 'maven:latest'
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
		  echo *generando los test*
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
