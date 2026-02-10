pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                git 'https://github.com/nagarajucsd/Java_app_3.0.git'
            }
        }

        stage('Hello') {
            steps {
                echo 'Code downloaded successfully!'
            }
        }
    }
}
