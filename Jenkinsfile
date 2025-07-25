pipeline {
    agent any
    stages {
        stage('Deploy by tag') {
            when {
                expression {
                    def tag = sh(script: "git tag --points-at HEAD", returnStdout: true).trim()
                    return tag != ""
                }
            }
            steps {
                script {
                    def tag = sh(script: "git tag --points-at HEAD", returnStdout: true).trim()
                    echo "🚀 Deploying from tag: ${tag}"
                }
            }
        }
        stage('Skip if not a tag') {
            when {
                expression {
                    def tag = sh(script: "git tag --points-at HEAD", returnStdout: true).trim()
                    return tag == ""
                }
            }
            steps {
                echo "⏩ No tag found, skipping deployment"
            }
        }
    }
}

