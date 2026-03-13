pipeline {
    agent any

    parameters {
        string(name: 'BRANCH', defaultValue: 'dev', description: 'Branch Name')
    }

    stages {

        stage('Build - Dev') {
            when {
                expression { params.BRANCH == 'dev' }
            }
            steps {
                echo "Running DEV build"
            }
        }

        stage('Test - QA') {
            when {
                expression { params.BRANCH == 'qa' }
            }
            steps {
                echo "Running QA tests"
            }
        }

        stage('Deploy - Main') {
            when {
                expression { params.BRANCH == 'main' }
            }
            steps {
                echo "Deploying to Production"
            }
        }

    }
}
