pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o main/hello_exec main/hello.cpp'
            }
        }

        stage('Test') {
            steps {
                sh './main/hello_exec'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment Stage - Success!'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
