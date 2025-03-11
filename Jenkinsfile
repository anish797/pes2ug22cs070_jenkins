pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Intentional error: using a non-existent compiler
                    sh 'nonexistent_compiler -o pes2ug22cs070-1 main.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Running the compiled executable to print output
                    sh './pes2ug22cs070-1'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Add your deployment steps here if applicable
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
