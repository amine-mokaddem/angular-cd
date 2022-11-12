pipeline {
    agent any
    stages {
             stage("npm install") {
            steps {
                script {
                   sh 'npm install '
                }
            }
        }
         stage("building app") {
            steps {
                script {
                   sh 'ansible-playbook ansible/build.yml  -i ansible/inventory/host.yml -e "ansible_sudo_pass=12345678" -vvv'
                }
            }
        }
    }   
}
