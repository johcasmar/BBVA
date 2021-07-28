pipeline {
    agent {
        docker {
            image 'maven:3.8.1-adoptopenjdk-11' 
            args '-v /root/.m2:/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
		stage('Test') { 
            steps {
                sh 'mvn test' 
            }
        }
		/*stage('Sonar') { 
            steps {
                sh ('''mvn sonar:sonar \
				-Dsonar.projectKey=bbva \
				-Dsonar.host.url=http://35.224.61.71:9000 \
				-Dsonar.login=2a9b416aac3490275cc7f2e3bb0397810ea49cae
				''')
            }
        }*/
		stage('Deploy') { 
            steps {
                sh 'java -jar /var/jenkins_home/workspace/java-app/target/my-app-1.0-SNAPSHOT.jar' 
            }
        }
    }
}
