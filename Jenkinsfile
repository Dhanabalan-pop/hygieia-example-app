pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                sh './gradlew build'
            }
        }
        stage('SonarQube') {
            steps {
                // sh './gradlew -Dsonar.host.url=http://sonarqube:9000 jacocoTestReport sonarqube'
                   sh ./gradlew sonarqube -Dsonar.projectKey=Test -Dsonar.host.url=http://54.67.83.8:9000 -Dsonar.login=02bf617eea1a51cf88d0ad008e9ecf18e15e1f4a
            }
        }
    }
}
