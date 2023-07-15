pipeline {
    agent any
    stages{
        stage("mvn-build") {
            steps{
                sh "mvn clean package" 
            }
        }
        stage("slacknotification"){
            steps{
                post {
                    always {
                        slackSend channel: '#jenkins-intigration', message: "This build is scucess on ${JOB_NAME}-${BUILD_NUMBER}"
                    }
                }
            }
         }  
    }
}