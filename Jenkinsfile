pipeline {
    agent any

    tools {
        maven "maven"
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }

            post {
                success {
                    echo "build failure"
                }
                failure {
                    echo "build failure"
                }
            }
        }
    }
}
