pipeline {
    agent any
    

    stages {
        stage('dry-run') {
            steps {
                sh "env"
                sh "echo hi"
                sh "ansible-playbook roboshop-dryrun.yml -e COMPONENT=mongodb -i inv -e ansible_user=${SSH_CRED_USR} -e ansible_password=${SSH_CRED_PSW}"  
            }
        }
    }
}

