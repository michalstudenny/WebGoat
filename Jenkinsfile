pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('SonarQube analysis') {
            steps {
                withSonarQubeEnv('sonarcloud') {
                    sh 'mvn sonar:sonar'
                }
            }
        }
    }
}
