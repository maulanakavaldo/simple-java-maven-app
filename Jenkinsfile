pipeline {
    agent {
        image 'maven:3.6.0-jdk-13'
        label 'docker'
    }
    stages {
        stage('Build') {
            steps {
                sh "mvn clean install"
            }
        }
    }
    post {
        always {
            cleanWs()
        }
    }
}
