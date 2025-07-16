#!/usr/bin/env groovy

pipeline {
    agent any
    stages {
        stage('test') {
            steps {
                script {
                    echo "Testing the application"
                    checkout scmGit(branches: [[name: '*/jenkins-jobs']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-pat-token', url: 'https://github.com/AmirPyDev/java-maven-app.git']])
                }
            }
        }
        stage('build') {
            when {
                expression {
                    return env.BRANCH_NAME == 'main'
                }
            }
            steps {
                script {
                    echo "Building the application..."
                }
            }
        }
        stage('deploy') {
            when {
                expression {
                    return env.BRANCH_NAME == 'main'
                }
            }            
            steps {
                script {
                    echo "Deploying the application..."
                }
            }
        }
    }
}
