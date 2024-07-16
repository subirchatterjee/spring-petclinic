pipeline {
    agent any

    stages {
        stage('MavenPackage') {
            steps {
                   
                sh './mvnw package'

            }
        }

        stage('DockerBuild') {
            steps {
                     
                    sh 'docker build -t vaskar20222/springpetclinic:latest .'
                   }
           }

        stage('Imagepush') {
            steps {
                     
                    sh 'docker push vaskar20222/springpetclinic:latest '
                   }
           }

      }
   
   }


