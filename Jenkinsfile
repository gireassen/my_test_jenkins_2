pipeline {
    agent any
    stages {
        stage('Build if Tag Exists') {
            when {
                expression {
                    def tag = sh(script: 'git tag --points-at HEAD', returnStdout: true).trim()
                    return tag != ''
                }
            }
            steps {
                echo "Release tag found. Deploying: ${tag}"
            }
        }
    }
}

