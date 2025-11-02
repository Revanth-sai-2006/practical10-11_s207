pipeline {
    agent any
    stages {
        stage('Run Ansible') {
            steps {
                bat 'wsl ansible-playbook -i inventory.yml playbook.yml'
            }
        }
    }
}
