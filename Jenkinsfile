pipeline {
    agent any

    environment {
        IMAGE_NAME = "sunnyajy293/ajay-demo"
    }

    stages {

        stage('Run Script') {
            steps {
                sh 'chmod +x hello.sh'
                sh './hello.sh'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t $IMAGE_NAME .'
            }
        }

        stage('Push Image to DockerHub') {
            steps {
                sh 'docker push $IMAGE_NAME'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run $IMAGE_NAME'
            }
        }

    }
}
