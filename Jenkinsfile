pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Running build for ${env.BRANCH_NAME} environment"
            }
        }

        stage('Deploy') {
            when {
                expression {
                    return env.BRANCH_NAME in ['Dev', 'QA', 'UAT', 'Prod']
                }
            }
            steps {
                echo "Deploying to ${env.BRANCH_NAME} environment"
                // Add deployment steps here
            }
        }
    }
}
