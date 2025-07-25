pipeline {
    agent any
    triggers {
        githubPush()
    }
    stages {
        stage('Check if tag') {
            when {
                expression {
                    def tag = sh(script: 'git tag --points-at HEAD', returnStdout: true).trim()
                    return tag != ''
                }
            }
            steps {
                echo "Tag detected, starting production deploy."
            }
        }
        stage('Skip if not tag') {
            when {
                expression {
                    def tag = sh(script: 'git tag --points-at HEAD', returnStdout: true).trim()
                    return tag == ''
                }
            }
            steps {
                echo "No tag detected. Skipping production deployment."
            }
        }
    }
}

