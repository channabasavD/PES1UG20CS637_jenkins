pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o this is error'
                sh 'g++ -o PES1UG20CS637 PES1UG20CS637.cpp'
                build job : 'PES1UG20CS637-1'
                echo 'Build Successful'
            }
        }
        stage('Test') {
            steps {
                sh './PES1UG20CS637'
                echo 'Test Successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }
    post {
        failure {
          echo 'Pipeline failed'
                }
            
        
    }
}
