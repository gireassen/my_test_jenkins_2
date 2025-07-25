pipeline {
    agent any
    stages {
        stage('Deploy by tag only') {
            when {
                expression {
                    def tag = sh(script: 'git tag --points-at HEAD', returnStdout: true).trim()
                    return tag != ''
                }
            }
            steps {
                script {
                    def tag = sh(script: 'git tag --points-at HEAD', returnStdout: true).trim()
                    echo "Deploying production tag: ${tag}"
                    // деплой на прод
                    sh "echo 'Deploying tag ${tag}'"
                }
            }
        }
    }
}
