pipeline {
    agent any
    stages {
        stage('SCM') {
            steps {
                git 'https://github.com/foo/bar.git'
            }
            
        }
        stage('SonarQube analysis') {
            steps {
                withSonarQubeEnv(installationName: 'sonarqube') {
                    sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.7.0.1746:sonar'
            }
            }
            
        }
    }
}
