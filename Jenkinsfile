pipeline {
    agent any

    stages {
        stage('Tag Detected') {
            when {
                expression { return env.ref_type == 'tag' }
            }
            steps {
                script {
                    echo "Triggered by tag: ${env.ref}"
                }
            }
        }
    }
}

