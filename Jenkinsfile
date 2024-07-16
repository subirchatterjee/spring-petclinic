pipeline {
    environment {
    registry = "swagatam04/spring-petclinic"
    registryCredential = 'dockerhub'
    AWS_ACCOUNT_ID="098974694488"
    AWS_DEFAULT_REGION="us-east-2"
    IMAGE_REPO_NAME="demo"
    REPOSITORY_URI = "${AWS_ACCOUNT_ID}.dkr.ecr.${AWS_DEFAULT_REGION}.amazonaws.com/${IMAGE_REPO_NAME}"


  }
    agent any

    stages {
        stage('Build') {
            steps {
                dir("/var/lib/jenkins/workspace/MAVENBUILD") {
                         sh './mvnw package'

                }
            }
        }
    }

