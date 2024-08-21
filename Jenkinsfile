pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning the repository...'
                // Clones the repository from GitHub
                git branch: 'main', url: 'https://github.com/talelekaustubh/opio.git'
                
                // List files in the workspace to verify the checkout
                sh 'ls -la'
            }
        }
        
        stage('Build') {
            steps {
                echo 'Building the Java project...'
                // Run the Maven build
                sh 'mvn clean compile'
            }
        }
        
        stage('Run') {
            steps {
                echo 'Running the Java application...'
                // Run the Java application
                sh 'java -cp target/classes HelloWorld'
            }
        }
    }
}