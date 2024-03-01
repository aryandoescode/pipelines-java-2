pipeline {
    agent any

    stages {
        stage('Preparation') {
            steps {
                git scm
                
            }
        }

        stage('Build') {
            steps {
                // Add your build commands, e.g., for Maven:
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                // Add your test commands, e.g., for Maven:
                sh 'mvn test'
            }
        }
    }

    post {
        always {
            // Cleanup or additional steps to run always
        }
        success {
            // Actions to take on success
            emailext(
                subject: "Build Successful: ${currentBuild.fullDisplayName}",
                body: "The build ${currentBuild.fullDisplayName} was successful.",
                to: "aryanhungry8@gmail.com",
                replyTo: "jenkins@example.com",
                mimeType: 'text/html'
            )
        }
        failure {
            // Actions to take on failure
            emailext(
                subject: "Build Failed: ${currentBuild.fullDisplayName}",
                body: "The build ${currentBuild.fullDisplayName} failed. Please investigate.",
                to: "aryanhungry8@gmail.com",
                replyTo: "jenkins@example.com",
                mimeType: 'text/html'
            )
        }
    }
}
