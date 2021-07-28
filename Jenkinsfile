pipeline {
    agent any
	 tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M3"
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
        }
                stage('Push') {
            steps {
                sh ('''
                   echo push
                   ''')
            }
        }
        stage('Deploy') {
             steps {
                sh ('''
                   echo ********************
		   echo *Desplegando el jar*
		   echo ********************
		   java -jar /var/jenkins_home/workspace/m/target/my-app-1.0-SNAPSHOT.jar
                   ''')
            }
         }
      }
   }
