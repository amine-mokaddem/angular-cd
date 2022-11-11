pipeline {
    agent any
    stages {
         stage("building app") {
            steps {
                script {
                   sh ' ansible-playbook ansible/build.yml  -i ansible/inventory/host.yml -e "ansible_become_password=12345678" '
                }
            }
        }
    }   
}
