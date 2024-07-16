pipeline {
    
    agent any

    stages {
       
        stage('Build') {
            steps {
                dir("/var/lib/jenkins/workspace/MAVENBUILD") {
                         sh './mvnw package'

                }
            }
        }
