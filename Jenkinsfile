pipeline {
    agent any
    
    environment {
        
        registry = "vaskar20222/petclinic"
        registryCredential = 'vaskar20222'        
    }

    stages {
        stage('MavenPackage') {
            steps {
                   
                sh './mvnw package'

            }
        }

        stage('DockerBuild') {
            steps {
                     
                    sh 'docker build -t vaskar20222/myclinic1:latest .'
                   }
           }

        stage('Imagepush') {
            steps {
                     
                    sh 'docker push vaskar20222/myclinic1:latest'
                   }
           }

      }
   
   }


