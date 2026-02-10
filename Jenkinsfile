pipeline {
    agent any
    tools {
        maven Maven3
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
    }
}
