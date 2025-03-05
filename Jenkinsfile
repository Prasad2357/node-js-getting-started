pipeline {
    agent any
 
    environment {
        NODE_HOME = tool('NodeJS')  // Correct way to define tool
        PATH = "${NODE_HOME}/bin:${env.PATH}" // Proper PATH assignment
    }
 
    stages {
        stage('Install Dependencies') {
            steps {
                powershell 'npm install' // Use sh 'npm install' for Linux
            }
        }
 
        stage('Build') {
            steps {
                powershell 'npm run build' // Use sh 'npm run build' for Linux
            }
        }
 
        stage('Test') {
            steps {
                powershell 'npm test' // Use sh 'npm test' for Linux
            }
        }
 
        stage('Deploy') {
            steps {
                powershell 'npm start' // Use sh 'npm start' for Linux
            }
        }
    }
}
