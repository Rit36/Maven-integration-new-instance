pipeline {
tools{
       jdk 'JAVA_HOME_UBU'
	   maven 'M2_HOME_UBU'
	   
}
    agent {label 'winslave'}

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Rit36/Maven-integration.git'
            }
        }
    stage('compile') {
            steps {
               sh 'mvn compile'
            }
        }
		   stage('test') {
            steps {
               sh 'mvn test'
            }
        }

		
   stage('package') {
            steps {
               sh 'mvn package'
            }
        }


    }
}
