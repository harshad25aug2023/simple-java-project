pipeline {
    agent any
    stages {
        stage("git checkout") {
            steps {
                git credentialsId: 'harshad25aug2023', url: 'https://github.com/buddy-works/simple-java-project'
            }
        }
        stage('clean and install') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('clean and package') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('go inside the folder') {
            steps {
                sh 'cd target/'
                sh 'ls -l'
            }
        }
        stage('again go inside the target directory') {
            steps {
                 sh 'cd target/'
                 sh 'cat pom.xml'
            }
        }
    }
}
