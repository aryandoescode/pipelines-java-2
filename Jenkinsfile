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
                mail bcc: '', body: 'Hello', cc: '', from: '', replyTo: '', subject: '', to: 'aryanhungry8@gmail.com'
            }
        }
        stage('Mail') {
            steps {
                // Add your test commands, e.g., for Maven:
                mail bcc: '', body: 'Hello', cc: '', from: '', replyTo: '', subject: '', to: 'aryanhungry8@gmail.com'
            }
        }
    }

    
    }

