#!/usr/bin/env groovy

pipeline {
    
    agent {
        docker {
            image 'node'
            label 'my-defined-label'
            args '-u root'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'npm test'
            }
        }
    }
}
