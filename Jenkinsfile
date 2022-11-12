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
                   sh 'sudo ansible-playbook ansible/build.yml  -i ansible/inventory/host.yml -vvv'
                }
            }
        }
    }   
}
