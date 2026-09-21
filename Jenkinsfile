pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building from Jenkinsfile'
                sh 'java -version'
                sh 'mvn -version'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing from Jenkinsfile'
            }
        }

        stage('Credentials Test') {
            steps {
                withCredentials([string(credentialsId: 'practice-secret', variable: 'MY_SECRET')]) {
                    sh 'echo "Credential received successfully"'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying from Jenkinsfile'
            }
        }
    }
}
