pipeline {
    agent any
    environment {
        NODE_HOME = tool name: 'NodeJS', type: 'NodeJSInstallation'  // Make sure 'NodeJS' is the name of the tool configured in Jenkins
        PATH = "${NODE_HOME}/bin:${env.PATH}"  // Reference NODE_HOME without 'env.'
    }
    stages {
        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }
        stage('Build') {
            steps {
                bat 'npm run build'
            }
        }
        stage('Test') {
            steps {
                bat 'npm test'
            }
        }
        stage('Deploy') {
            steps {
                bat 'npm start'
            }
        }
    }
}
