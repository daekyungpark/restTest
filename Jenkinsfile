pipeline {
    agent any
    stages {
        stage('build') {
            steps {
				sh "pwd"
				sh "ls -al"
				sh "java -version"				
				sh 'chmod +x gradlew'
				sh "./gradlew clean build -x test"	
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