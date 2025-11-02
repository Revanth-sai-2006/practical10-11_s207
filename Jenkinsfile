pipeline {
    agent any

    stages {

        stage('Checkout SCM') {
            steps {
                checkout scm
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                // Ensure we’re in the right workspace and files exist
                dir("${WORKSPACE}") {
                    bat '''
                        echo Current directory: %cd%
                        echo Listing files...
                        dir
                        
                        echo Running Ansible playbook...
                        wsl ansible-playbook -i inventory.yml playbook.yml
                    '''
                }
            }
        }
    }

    post {
        success {
            echo '✅ Ansible playbook executed successfully!'
        }
        failure {
            echo '❌ Build failed — check console output for details.'
        }
    }
}
