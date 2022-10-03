pipeline {
    agent any
    environment {
        SSH_CRED = credentials('SSH')
    }

    stages {
        stage('dry-run') {
            steps {
                sh "echo hi"
            }
        }
    }
}