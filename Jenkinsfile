pipeline {
    agent any
    tools {
        maven 'Maven3'
    }
    environment {
        APP_NAME = "MyFirstApp"
    }
    stages {

        stage('Checkout Code') {
            steps {
                git branch:'main', url: 'https://github.com/nagarajucsd/Java_app_3.0.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Test'){
            steps{
                sh 'mvn test'
            }
        } 
        stage('app name') {
            echo 'App name is :{$APP_NAME}'
        }
    }
    post {
        success{
            echo 'build and test successful'
        }
        failure {
            echo 'build and test failed'
        }
    }
}
