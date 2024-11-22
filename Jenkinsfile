pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Pulls the code from GitHub
                git credentialsId: 'github-token', url: 'https://github.com/Genda-phool/jk.git', branch: 'main'
            }
        }
        stage('Build') {
            steps {
                // Run your build script here
                sh './mvnw clean install'  // For Maven-based projects
            }
        }
        stage('Test') {
            steps {
                // Run tests
                sh './mvnw test'
            }
        }
        stage('Deploy') {
            steps {
                // Deploy the application (if needed)
                sh './deploy.sh'  // Replace with your deployment script
            }
        }
    }
}
