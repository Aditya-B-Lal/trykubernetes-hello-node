pipeline {
    agent any
    
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
         stage('Build Docker Image') {
            steps {
                script {
                  sh 'docker build -t kubernetestry .'
                }
            }
        }
        
        stage('Deploy Docker Image') {
            steps {
                script {
                     
                    sh 'docker login -u 9526584898 -p Aditya123*'
                    sh 'docker tag kubernetestry 9526584898/minikube:kubernetestry'
                    sh 'docker push 9526584898/minikube:kubernetestry'
                }
            }
        }
    }
}
 
