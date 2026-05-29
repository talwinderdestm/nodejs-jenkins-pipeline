pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm run build'
                echo 'Build completed'
            }
        }

        stage('Lint') {
            steps {
                sh 'npm run lint'
                echo 'Lint completed'
            }
        }

        stage('Test') {
            steps {
                sh 'npm run test'
                echo 'Test completed'
            }
        }
    }

    post {
        success {
            echo 'Build, Lint, and Test completed successfully'
        }
        
        failure {
            echo 'Build, Lint, and Test failed'
        }
    }
}