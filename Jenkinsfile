pipeline {
    agent any
    stages{
        stage("mvn-build") {
            steps{
                sh "mvn clean package" 
            }
        }
    }
}