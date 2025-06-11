@Library('first-library') 
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
    }
}