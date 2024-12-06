pipeline {
    agent {
        node {
            label 'nodejs'
        }
    }
    stages {
        stage('Run Tests') {
            parallel {
                stage('Backend Tests') {
                    steps {
                        sh 'node ./simple-webapp/backend/test.js'
                    }
                }
                stage('Frontend Tests') {
                    steps {
                        sh 'node ./simple-webapp/frontend/test.js'
                    }
                }
            }
        }
    }
}
