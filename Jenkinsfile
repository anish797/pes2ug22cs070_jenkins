pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Compiling hello.cpp...'
                    sh '''
                    g++ -o pes2ug22cs070-1 main/hello.cpp
                    '''
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    echo 'Running hello.cpp output...'
                    sh '''
                    ./pes2ug22cs070-1
                    '''
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    echo 'Deploy stage placeholder'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
