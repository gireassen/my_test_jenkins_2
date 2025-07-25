pipeline {
    agent any
    stages {
        stage('Deploy production only if tagged') {
            when {
                expression {
                    def tag = sh(script: 'git tag --points-at HEAD', returnStdout: true).trim()
                    return tag != ''
                }
            }
            steps {
                echo "Production tag detected. Deploying release!"
            }
        }
    }
}
