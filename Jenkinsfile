#!/usr/bin/env groovy

pipeline {
    agent none
    stages {
        stage('test') {
            steps {
                script {
                    echo "Testing the application..."
                    echo "Testing the application..."
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
