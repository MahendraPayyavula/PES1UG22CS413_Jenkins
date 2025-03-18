pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o output PES1UG22CS413.cpp'  // Compiling C++ file
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './output'  // Running compiled C++ file
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment Step '
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
