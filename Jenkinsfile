pipeline {
    agent any

    stages {
        stage('Run Ansible Playbook') {
            steps {
                bat '''
                wsl ansible-playbook -i /mnt/c/ProgramData/Jenkins/.jenkins/workspace/Ansibledeployment/inventory.yml /mnt/c/ProgramData/Jenkins/.jenkins/workspace/Ansibledeployment/playbook.yml
                '''
            }
        }
    }
}
