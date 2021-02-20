pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Build docker Image') {
            steps {
                echo 'Hello new Stage'
                echo "THE NUMBER IS ${env.BUILD_NUMBER}"            
                sh "docker build -t benjaminsh/hello-world-jenkins:v${env.BUILD_NUMBER} ."
                sh "docker push benjaminsh/hello-world-jenkins:v${env.BUILD_NUMBER}"
            }
        }
    }
}
