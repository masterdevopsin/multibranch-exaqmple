pipeline {
    agent any

    stages {

        stage('Debug Branch') {
            steps {
                echo "Current Git Branch: ${env.GIT_BRANCH}"
            }
        }

        stage('Build - Dev') {
            when {
                expression { env.GIT_BRANCH == 'origin/dev' }
            }
            steps {
                echo "Running DEV build"
                echo "hi "
                
            }
        }

        stage('Test - QA') {
            when {
                expression { env.GIT_BRANCH == 'origin/qa' }
            }
            steps {
                echo "Running QA tests"
            }
        }

        stage('Deploy - Main') {
            when {
                expression { env.GIT_BRANCH == 'origin/main' }
            }
            steps {
                echo "Deploying to Production"
            }
        }

    }
}
