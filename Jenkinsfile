pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/https://github.com/Revanth-sai-2006/practical10-11_s207.git//ansible-playbooks.git'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                sh '''
                ansible-playbook -i inventory.yml playbook.yml
                '''
            }
        }
    }
}
