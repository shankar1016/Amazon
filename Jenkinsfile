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
                dir ('SKY') {
                sh 'mvn compile'
            }
        }
    }

        stage('test') {
            steps {
                dir ('SKY') {
                sh 'mvn test'
            }
        }
    }

        stage('build') {
            steps {
                dir ('SKY') {
                sh 'mvn clean install'
            }
        }
    }
}
}
