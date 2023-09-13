pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit and integration tests...'
            }
            post {
                success {
                    emailext body: 'Unit and integration tests were successful!', subject: 'Stage Success: Unit and Integration Tests', to: 'lovepreet.singh10235@gmail.com'
                }
                failure {
                    emailext body: 'Unit and integration tests failed. Please check logs.', subject: 'Stage Failure: Unit and Integration Tests', to: 'lovepreet.singh10235@gmail.com'
                }
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Performing code analysis...'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Performing security scan...'
            }
            post {
                success {
                    emailext body: 'Security scan was successful!', subject: 'Stage Success: Security Scan', to: 'lovepreet.singh10235@gmail.com'
                }
                failure {
                    emailext body: 'Security scan failed. Please check logs.', subject: 'Stage Failure: Security Scan', to: 'lovepreet.singh10235@gmail.com'
                }
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging environment...'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging...'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production environment...'
            }
        }
    }

    post {
        success {
            emailext body: 'The pipeline was successful!', subject: 'Pipeline Success', to: 'lovepreet.singh10235@gmail.com'
        }
        failure {
            emailext body: 'The pipeline failed. Please check logs.', subject: 'Pipeline Failure', to: 'lovepreet.singh10235@gmail.com'
        }
    }
}
