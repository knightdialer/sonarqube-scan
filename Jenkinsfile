pipeline {
    agent any
    stages {
        stage('SCM') {
            steps {
                git branch: 'main', url: 'https://github.com/knightdialer/sonarqube-scan.git'
            }
            
        }
        stage('SonarQube analysis') {
            steps {
                withSonarQubeEnv(installationName: 'sonarqube') {
                    sh 'mvn clean verify sonar:sonar'
            }
            }
            
        }
    }
}
