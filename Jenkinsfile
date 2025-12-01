pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                echo 'Running build and sending test email.....'
            }
        }
       }
    post{
        success{
            emailext(
                to: "ranu.vish22@gmail.com",
                subject: "Build SUCCESS",
                body: "Build URL: ${BUILD_URL}"
                )
        }
        failure{
            emailext(
                to: "ranu.vish22@gmail.com",
                subject: "Build FAILED ",
                body: "Build URL: ${BUILD_URL}"
                )
        }
    }
}
