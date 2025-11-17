pipeline {
    agent any

    environment {
        NODE_OPTIONS = "--openssl-legacy-provider"
        CI = "false"        // 🚀 Disable warnings as errors
    }

    stages {
        stage('Git checkout') {
            steps {
                git 'https://github.com/sravandevops09/Trading-UI.git'
            }
        }

        stage('Install npm prerequisites') {
            steps {
                sh '''
                    npm install
                    npm run build
                '''
            }
        }
    }
}
