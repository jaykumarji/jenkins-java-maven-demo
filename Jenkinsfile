
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build and Test') {
            steps {
                sh 'java -version'
        sh 'mvn -version'
        sh 'echo $JAVA_HOME'
        sh 'which java'
        sh 'which javac'
        sh 'javac -version'
        sh 'mvn -B clean verify'
            }
        }
    }

    post {
        success {
            echo 'SUCCESS: Java build and tests passed!'
        }
        failure {
            echo 'FAILURE: Check the console output.'
        }
    }
}
