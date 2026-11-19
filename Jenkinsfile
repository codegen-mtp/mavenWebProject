pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps { checkout scm }
        }
        stage('Maven Build') {
            steps {
                bat 'mvn clean package'
            }
        }
    }
    post {
        success { echo 'Maven web application built successfully.' }
        failure { echo 'Maven web application build failed.' }
    }
}
