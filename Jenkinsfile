pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                echo "Cloning repository..."
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo "Building the project..."
                // Add your build commands here
                // Example for Java: sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                echo "Running tests..."
                // Add your test commands here
                // Example: sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying the project..."
                // Add your deploy steps here
                // Example: sh './deploy.sh'
            }
        }
    }
    post {
        success {
            echo "Pipeline completed successfully ✅"
        }
        failure {
            echo "Pipeline failed ❌"
        }
    }
}
