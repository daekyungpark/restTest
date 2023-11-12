pipeline {
    agent any
    stages {
		stage('Git Progress') {
			steps {
				git credentialsId: 'github_personal_access_token', 
				url: 'https://github.com/daekyungpark/restTest.git'
			  }
			}
		stage('Gradle Build') {
			  steps {
				sh 'gradle clean build -x test -b build-server.gradle'
			  }
		}
        stage('build') {
            steps {
				sh "pwd"
				sh "ls -al"
				sh "java -version"				
				sh 'chmod +x gradlew'
				sh "./gradlew clean bootjar"	
				sh "ls -al"
				sh "ls -al ./build"			
				sh "ls -al ./build/libs"					
				sh "ls -al ./build/classes/java/main"		
				sh "ls -al ./src/main/java"
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
                echo 'deploying the application...'
            }
        }
    }
}