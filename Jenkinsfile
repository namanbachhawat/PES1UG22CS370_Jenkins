pipeline {
    agent any
    
    stages {
        stage('Clone Repository') {
            steps {
                script {
                    sh 'git clone https://github.com/namanbachhawat/PES1UG22CS370_Jenkins.git'
                }
            }
        }
        
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES1UG22CS370-1 PES1UG22CS370_Jenkins/working.cpp'
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    sh './PES1UG22CS370-1'
                }
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'deploy'
                // Add deployment steps here
            }
        }
    }
    
    post {
        failure {
            echo 'pipeline failed'
        }
    }
}
