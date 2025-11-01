pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Revanth-sai-2006/practical10-11_s207.git'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                bat '''
                ansible-playbook -i inventory.yml playbook.yml
                '''
            }
        }
    }
}
