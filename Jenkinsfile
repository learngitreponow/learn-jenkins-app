pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker{
                    image 'node:18-alpine'
                    reuseNODE true
                }
            }
            steps {
                sh '''
                    ls -la
                    node --verion
                    npm --version
                    npm ci
                    npm run build
                    ls -la 
                '''
            }
        }
    }
}
