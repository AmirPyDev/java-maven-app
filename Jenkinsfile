#!/usr/bin/env groovy

pipeline {
    agent any
    stages {
        stage('test') {
            steps {
                script {
                    echo "Testing the application with github-creds"
                    
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
