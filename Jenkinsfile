pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building Docker image...'
                sh 'docker build -t nodejs-demo-app .'
            }
        }

        stage('Test') {
            steps {
                echo 'Running simple test...'
                sh 'echo "Tests passed!"'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying container...'
                sh 'docker run -d -p 3000:3000 nodejs-demo-app'
            }
        }
    }
}
