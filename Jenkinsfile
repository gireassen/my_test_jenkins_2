pipeline {
    agent any
    triggers {
        githubPush()
    }
    stages {
        stage('Dev: Build') {
            steps {
                echo "Building development branch: ${env.GIT_BRANCH}"
            }
        }
        stage('Dev: Test') {
            steps {
                echo "Running tests for development branch"
            }
        }
    }
}

