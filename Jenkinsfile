pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES2UG22CS371 main/hello.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES2UG22CS371'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
