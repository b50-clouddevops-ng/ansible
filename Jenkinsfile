pipeline {
    agent any
    environment {
        SSH_CRED = credentials('SSH_NG')
    }

    stages {
        stage('dry-run') {
            steps {
                sh "env"
                sh "ansible-playbook -i inv roboshop-dryrun.yml -e COMPONENT=mongodb -e ansible_password=DevOps321 -e ansible_user=${SSH_CRED_USR} "
            }
        }
    }
}

