pipeline {
    agent any

    tools {
        maven 'maven'
    }

    stages {

        stage('Git Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/VenkateshJaggaraju/maven_projects.git'
            }
            post {
                success {
                    echo "Pull SUCCESS"
                }
                failure {
                    echo "Pull FAILED"
                }
            }
        }

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
