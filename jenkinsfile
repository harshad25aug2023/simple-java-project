pipeline {
    agent any
    stages {
        stage('Git Checkout') {
            steps {
                git credentialsId: 'harshad25aug2023', url: 'https://github.com/buddy-works/simple-java-project'
            }
        }
        stage('Clean and Install') {
            steps {
                sh 'mvn clean'
                sh 'mvn install'  // Fix the typo here (from 'man install' to 'mvn install')
            }
        }
    }
}
