pipeline {
    agent any
    environment {
        CI = 'true'
        PATH = "/usr/bin/npm:${env.PATH}"
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}
