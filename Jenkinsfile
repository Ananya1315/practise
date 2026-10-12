pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                bat 'mvn clean package'
            }
        }
        stage('Test'){
            steps{
                bat 'mvn test'
            }
        }
        stage('Docker build'){
            steps{
                bat 'docker build -t student-java-app .'
            }
        }
        stage('Docker Run'){
            steps{
                bat 'docker run -d -p 8081:8080 student-java-app .'
            }
        }
    }
}