pipeline {
    agent any

    stages {

        stage('Run Script') {
            steps {
                sh 'chmod +x hello.sh'
                sh './hello.sh'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t ajay-demo .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run ajay-demo'
            }
        }

    }
}
