pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/tthunt04/springboot-webapp.git'
            }
        }

        stage('Build Jar') {
            steps {
                bat 'mvnw clean package -DskipTests'
            }
        }

        stage('Push to Nexus') {
            steps {
                echo 'This step pushes the built jar file to Nexus repository.'
            }
        }
    }
}