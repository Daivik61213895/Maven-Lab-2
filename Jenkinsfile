pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Checkout your source code from version control
                git branch 'master' 'https://github.com/hkshitesh/SL-CICD-MAVEN-18-JAN.git'
            }
        }
        stage('Build') {
            steps {
                // Use Maven to build your project
                bat 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                // Run tests if applicable
                bat 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Delpoy Successfully'
                // Deploy your artifact, if necessary
                // Example: sh 'mvn deploy'
            }
        }
    }
    

    post {
        success {
            // This block will be executed if the pipeline runs successfully
            echo 'Pipeline executed successfully!'
        }
        failure {
            // This block will be executed if the pipeline fails
            echo 'Pipeline failed!'
        }
    }
}
