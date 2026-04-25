pipeline {
    agent any

    tools {
        maven 'Maven'   // make sure Maven is configured in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/ArSrini27/devopslab.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
