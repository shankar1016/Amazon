pipeline {
    agent any 

    stages {
        stage('Clone_project') {
            steps {
                git branch: 'master', url: 'https://github.com/shankar1016/Amazon.git'
            }
        }

        stage('compile') {
            steps {
                dir ('Amazon') {
                sh 'mvn compile'
            }
        }
    }

        stage('test') {
            steps {
                dir ('Amazon') {
                sh 'mvn test'
            }
        }
    }

        stage('build') {
            steps {
                dir ('Amazon') {
                sh 'mvn clean install'
            }
        }
    }
}
}
