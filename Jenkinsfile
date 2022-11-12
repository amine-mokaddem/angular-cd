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
                   sh 'sudo ansible-playbook ansible/build.yml  -i ansible/inventory/host.yml'
                }
            }
        }
         stage("create & run docker image ") {
            steps {
                script {
                   sh 'sudo ansible-playbook ansible/docker.yml  -i ansible/inventory/host.yml'
                }
            }
        }
         stage("docker login & docker push") {
            steps {
                script {
                   sh 'sudo ansible-playbook ansible/docker-registry.yml  -i ansible/inventory/host.yml'
                }
            }
        }
    }   
}
