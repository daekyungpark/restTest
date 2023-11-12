pipeline {
    agent any
    stages {		
        stage('build') {
            steps {
				sh "pwd"
				sh "ls -al"
				sh "java -version"	
                echo 'building the application...'
            }
        }
        stage('test') {
            steps {
                echo 'testing the application...'
            }
        }
        stage('deploy') {
            steps {
			    sh "cp -rf Jenkinsfile /home/izttotio/backend"
                echo 'deploying the application...'
            }
        }
    }
}