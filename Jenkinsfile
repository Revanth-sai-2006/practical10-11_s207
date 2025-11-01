pipeline {
    agent any

    stages {
        stage('Run Ansible Playbook') {
            steps {
                sh '''
                echo "Running Ansible Playbook..."
                ansible --version
                ansible-playbook -i inventory.yml playbook.yml
                '''
            }
        }
    }
}
