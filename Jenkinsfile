pipeline {
    node {
        stage('SCM') {
            git 'https://github.com/knightdialer/sonarqube-scan.git'
        }
        stage('SonarQube analysis') {
            withSonarQubeEnv(installationName: 'sonarqube') { 
                sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.7.0.1746:sonar'
            }
        }
    }
}
