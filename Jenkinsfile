pipeline {
    agent any
    environment {
        App_Name ="Myapp"
    }
    tools{
        maven'Maven3'
    }
    stages {
        stage('git checkout'){
            steps{
                git branch:'main',url: 'https://github.com/nagarajucsd/Java_app_3.0.git'
            }
        }
        stage('build'){
            steps{
                sh 'mvn clean package'
            }
        }
        stage('test'){
            steps{
                sh 'mvn test'
        }
     }
        stage('app name'){
            steps{
                echo "App name is ${App_Name}"
            }
        }
        stage('artifact'){
            steps{
                archiveArtifacts artifacts: 'target/*.jar'
        }
    }
    }
 post{
     success{
         echo 'test success'
     }
     failure{
         echo 'test failure'
     }
 }

}
    
