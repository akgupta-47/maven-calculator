pipeline {
    agent {
        label 'master'
    }
    stages {
        stage('Build') {
            steps {
                bat 'mvn -B -DskipTests clean package'
            }
        }
        stage('Test') { 
            steps {
                bat 'mvn test' 
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml' 
                }
            }
        }
        stage('Custom-Reports') {
            steps {
                bat 'mvn site'
            }
        }
	  stage('video step') {
		steps {
			echo 'AKshat 101903781'
		}
	  }
    }
}