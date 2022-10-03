pipeline {
    agent any
    environment {
        SSH_CRED = credentials('SSH')
    }

    stages {
        stage('dry-run') {
            steps {
                sh "env"
                sh "ansible-playbook -i inv roboshop-dryrun.yml -e COMPONENT=mongodb -e ansible_user=${SSH_CRED_USR} -e ansible_password=${SSH_CRED_PSW}"
            }
        }
    }
}