pipeline {
    agent any
    stages{
        stage("mvn-build") {
            steps{
                sh "mvn clean package" 
            }
        }
        post {
                always {
                    slackSend channel: '#jenkins-intigration', message: "This build is scucess on ${JOB_NAME}-${BUILD_NUMBER}"
                    }
            }
    }
}