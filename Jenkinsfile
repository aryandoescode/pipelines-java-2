pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                // Add your build commands, e.g., for Maven
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
        success {
            // Actions to take on success
            emailext(
                mail bcc: '', body: 'The build ${currentBuild.fullDisplayName} was successful.', cc: '', from: '', replyTo: '', subject: '', to: 'aryanhungry8@gmail.com'
                
                
            )
        }
        failure {
                mail bcc: '', body: 'oooh yeah', cc: '', from: '', replyTo: '', subject: '', to: 'aryanhungry8@gmail.com'

            )
        }
    }
}
