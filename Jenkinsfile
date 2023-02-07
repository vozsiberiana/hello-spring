pipeline {
    agent any
    options { timestamps() }
    stages {
        stage('Package') {
            steps {
             ./mvnw package'
            }
        }

        stage('Build') {
            steps {
                sh 'docker-compose build'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker-compose up -d'
            }

        }
    }
}
