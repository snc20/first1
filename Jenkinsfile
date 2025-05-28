pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                echo 'Pipeline is working!'
            }
        }

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
