pipeline  {
    agent {
        docker {
            image 'node:18-alpine'
        }
    }

    stages {
        stage('Install') {
            steps {
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying (demo only)..."'
            }
        }
    }

    post {
        success {
            echo 'Pipline succeeded!'
        }
        failure {
            echo 'Pipline failed.'
        }
    }
}