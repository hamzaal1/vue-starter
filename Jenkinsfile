pipeline {
    agent any

    environment {
        NETLIFY_AUTH_TOKEN = credentials('netlify-auth-token') // Store your Netlify token in Jenkins credentials
    }

    stages {
        stage('Checkout') {
            steps {
                // Use credentialsId to access GitHub repository
                // git branch: 'main', url: 'https://github.com/your-username/your-repo.git', credentialsId: 'github-credentials'
                sh 'echo build'
            }
        }

        // stage('Install Dependencies') {
        //     steps {
        //         sh 'npm ci'
        //     }
        // }

        // stage('Build') {
        //     steps {
        //         sh 'npm run build'
        //     }
        // }

        // stage('Deploy to Netlify') {
        //     steps {
        //         withCredentials([string(credentialsId: 'netlify-auth-token', variable: 'NETLIFY_AUTH_TOKEN')]) {
        //             sh 'netlify deploy --prod --dir=dist'
        //         }
        //     }
        // }
    }
}
