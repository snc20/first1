pipeline {
    agent any

    environment {
        ANSIBLE_FORCE_COLOR = "true"
        ANSIBLE_HOST_KEY_CHECKING = "False"
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/<твій-юзернейм>/<репо>.git'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                sh 'ansible-playbook -i inventory/hosts.yml playbooks/site.yml -c local'
            }
        }
    }

    post {
        failure {
            echo 'Deployment failed.'
        }
        success {
            echo ' Ansible executed successfully.'
        }
    }
}
