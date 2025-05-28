pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Run Ansible') {
            steps {
                sh 'ansible-playbook -i inventory/hosts.yml playbooks/site.yml -K'
            }
        }
    }
}
