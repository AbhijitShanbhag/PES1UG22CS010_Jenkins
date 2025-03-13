pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'make -C main'
                echo 'Build Stage Successful'
            }
        }
        
        stage('Test') {
            steps {
                sh 'cd /var/jenkins_home/workspace/PES1UG22CS010/man/ && ./hello_exec'
                echo 'Test Stage Successful'
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
