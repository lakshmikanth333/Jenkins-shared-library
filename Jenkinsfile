@Library('first-library') _
pipeline {
    agent any
    
    stages {
        stage('local') {
            steps {
                script {
                    sh """
                    echo "This is the first shared library"
                    """
                }
            }
        }
        stage('library') {
            steps {
                firtstFunction()
            }
        }
        stage('trigger') {
            steps {
                build job: 'second', wait: false
            }
        }
    }
}