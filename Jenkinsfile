pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Building development branch: ${env.GIT_BRANCH}"
                // сборка, линт, тесты
                sh 'echo "Running tests..."'
            }
        }
    }
}
