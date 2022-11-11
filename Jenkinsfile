pipeline {
    agent any
    stages {
         stage("building app") {
            steps {
                script {
                   sh 'ansible all -m ping -i ansible/inventory'
 '
                }
            }
        }
    }   
}
