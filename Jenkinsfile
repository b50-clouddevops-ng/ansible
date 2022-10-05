pipeline {
    agent any
    environment {
        SSH_CRED = credentials('SSH_NG')
    }


    stages {
        stage('dry-run') {
            steps {
                sh "env"
                sh "ansible-playbook roboshop-dryrun.yml -e COMPONENT=mongodb -i inv -e ansible_user=${SSH_CRED_USR} -e ansible_password=${SSH_CRED_PSW}"  
            }
        }
    }
}

