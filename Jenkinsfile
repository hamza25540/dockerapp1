pipeline {
    agent any
    stages{
        stage('Test') {
            steps {
                sh 'docker build -t app1 .'
                sh 'docker run -d -p 5000:5000 --name app1 app1'
            }
        }
        stage('Build') {
            steps {
                sh 'touch example.txt'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo hello >> example.txt'
                sh 'cat example.txt'
            }
        }
    }
}