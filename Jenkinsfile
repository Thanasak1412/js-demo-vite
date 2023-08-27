pipeline {
    agent any

    tools {
        // Reference the Node.js installation configured in Jenkins
        nodejs "NodeJS-18.17.1"
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                // Install 'vite' globally
                sh 'npm install -g vite'
            }
        }

        stage('Build') {
            steps {
                // Run 'vite build' to build the React application
                sh 'vite build'
            }
        }

        // Add more stages as needed
    }
}
