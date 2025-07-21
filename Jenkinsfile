pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Building development branch: ${env.GIT_BRANCH}"
                // добавьте сюда сборку, тестирование, линтинг и т.д.
            }
        }

        stage('Unit Tests') {
            steps {
                echo "Running unit tests"
            }
        }
    }
}

