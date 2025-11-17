pipeline {
    agent any

    environment {
    NODE_OPTIONS="--openssl-legacy-provider"
}


    stages {
        stage('Git checkout') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/sravandevops09/Trading-UI.git'
                   }
}
        stage('Install npm prerequisites'){
            steps{
                sh'npm install'
                sh'npm run build'
                sh 'export NODE_OPTIONS=--openssl-legacy-provider && npm run build'

            }
        }
    }
}
