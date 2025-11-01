pipeline {
    agent any

    stages {
        stage('Run Ansible Playbook') {
            steps {
                bat '''
                ansible-playbook -i inventory.yml playbook.yml
                '''
            }
        }
    }
}
