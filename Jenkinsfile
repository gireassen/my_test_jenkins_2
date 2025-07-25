pipeline {
    agent any
    stages {
        stage('Check Branch') {
            steps {
                script {
                    def branch = params.BRANCH_NAME?.replace('refs/heads/', '')
                    if (branch != 'dev') {
                        error "This job only supports the 'dev' branch."
                    }
                    echo "Running job for branch: ${branch}"
                }
            }
        }

        stage('Build Dev') {
            steps {
                echo "This is the development build."
            }
        }
    }
}

