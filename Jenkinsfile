pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                echo 'executing npm...'
                nodejs(nodeJSInstallationName: 'NodeJS-18.17.1') {
                    sh 'npm install -g vite'
                }
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
