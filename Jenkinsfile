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
                dir ('SpringCore') {
                sh 'mvn compile'
            }
        }
    }

        stage('test') {
            steps {
                dir ('SpringCore') {
                sh 'mvn test'
            }
        }
    }

        stage('build') {
            steps {
                dir ('SpringCore') {
                sh 'mvn clean install'
            }
        }
    }
}
}
