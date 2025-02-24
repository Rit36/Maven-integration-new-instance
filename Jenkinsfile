pipeline {
tools{
       jdk 'JAVA_HOME_LIN'
	   maven 'M2_HOME_LIN'
	   
}
    agent {label 'linslave'}

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
