pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo '📦 Checking out code...'
                checkout scm
            }
        }
        stage('Build with Maven') {
            steps {
                echo '⚙️ Running Maven build...'
                sh 'mvn -B clean install'
            }
        }
    }
    post {
        success {
            echo '✅ Build successful!'
        }
        failure {
            echo '❌ Build failed!'
        }
    }
}

