#!/usr/bin/env groovy

pipeline {
    agent any
    stages {
        stage('test') {
            steps {
                script {
                    echo "Testing the application millionth times"
                    echo "Executing pipeline for branch ${env.BRANCH_NAME}"
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
                    echo "Deploying the application for multi branch"
                }
            }
        }
    }
}
