pipeline {
    agent any

    tools {
        maven "maven"
    }

    stages {
        stage('git repo'){
            steps {
                git branch:"master",url:"https://github.com/VenkateshJaggaraju/maven_projects.git"
            }
            post {
                success {
                    echo "pull SUCCESS"
                }
                failure {
                    echo "pull FAILED"
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
