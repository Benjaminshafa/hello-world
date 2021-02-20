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
                echo "Running ${VERSION} on ${env.JENKINS_URL}"            
                sh "docker build -t benjaminsh/hello-world-jenkins:${env.BUILD_ID} ."
                sh "docker push benjaminsh/hello-world-jenkins:${env.BUILD_ID}"
            }
        }
    }
}
