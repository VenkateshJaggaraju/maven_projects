pipeline {
    agent any
    tools {
        maven 'maven'
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }

            post {
                success {
                    echo "Build SUCCESS"
                }
                failure {
                    echo "Build FAILED"
                }
            }
        }
    }
}
