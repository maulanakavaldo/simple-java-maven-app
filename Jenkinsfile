pipeline {
    agent {
        image 'maven:3.9.9-jdk-17'
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
