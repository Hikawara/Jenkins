pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the code using Maven'
                // Actual build commands with Maven would go here
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running TestNG to ensure code functionality'
                // Commands to run unit tests would go here
                echo 'Running integration tests to ensure component interactions'
                // Commands to run integration tests would go here
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Integrating code analysis tool. Running SonarQube... '
                // Commands to run code analysis tool would go here
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Performing security scan on the code. Running OWASP ZAP... '
                // Commands to run security scan tool would go here
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying the Jenkins Deploy Plugin to staging server'
                // Commands to deploy to staging server would go here
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running Selenium on staging environment'
                // Commands to run integration tests on staging would go here
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying Jenkins Deploy Plugin'
                // Commands to deploy to production server would go here
            }
        }
    }

    post {
        success {
            echo 'Pipeline successfully completed!'
            emailext body: 'Pipeline successfully completed!',
                     subject: 'Pipeline Status: Success',
                     to: 'swanhtetnaingatwork@gmail.com',
                     attachmentsPattern: '**/*'
        }
        failure {
            echo 'Pipeline failed!'
            emailext body: 'Pipeline failed!',
                     subject: 'Pipeline Status: Failure',
                     to: 'swanhtetnaingatwork@gmail.com',
                     attachmentsPattern: '**/*'
        }
    }
}
