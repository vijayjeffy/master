pipeline {
    agent any

    stages {
        stage('Stage 1') {
            steps {
                echo 'Hello'
            }
        }

        stage('Stage 2') {
            steps {
                echo 'Hi'
            }
        }

        stage('Stage 3') {
            steps {
                echo 'How are you?'
            }
        }

        stage('Stage 4') {
            steps {
                echo 'I am fine'
            }
        }

        stage('Stage 5') {
            steps {
                echo 'Thank you'
            }
        }

        stage('Stage 6') {
            steps {
                echo 'Welcome'
            }
        }

        stage('Stage 7') {
            steps {
                echo 'Good Morning'
            }
        }

        stage('Stage 8') {
            steps {
                echo 'Good Evening'
            }
        }

        stage('Stage 9') {
            steps {
                echo 'Take care'
            }
        }

        stage('Stage 10') {
            steps {
                echo 'Bye'
            }
        }
    }

    post {
        success {
            emailext(
                subject: '✅ Jenkins Job Success',
                body: 'The pipeline has completed successfully!',
                to: 'aravindjenkin2@gmail.com'
            )
        }
        failure {
            emailext(
                subject: '❌ Jenkins Job Failed',
                body: 'The pipeline has failed!',
                to: 'aravindjenkin2@gmail.com'
            )
        }
    }
}
