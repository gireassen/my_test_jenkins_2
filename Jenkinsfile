pipeline {
    agent any

    stages {
        stage('Check tag') {
            when {
                expression {
                    def tag = sh(script: 'git tag --points-at HEAD', returnStdout: true).trim()
                    return tag != ''
                }
            }
            steps {
                echo "Tag found. Proceeding with release pipeline."
            }
        }

        stage('Deploy to Production') {
            when {
                expression {
                    def tag = sh(script: 'git tag --points-at HEAD', returnStdout: true).trim()
                    return tag != ''
                }
            }
            steps {
                echo "Deploying production version from tag"
                // сюда деплой
            }
        }
    }
}

