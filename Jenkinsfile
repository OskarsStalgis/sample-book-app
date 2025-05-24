pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                echo "Building of node application is starting.."
            }
        }
        stage('deploy-dev') {
            steps {
                echo "Deployment of node application on DEV environment.."
            }
        }
        stage('test-dev') {
            steps {
                echo "API test executuon against node application on DEV environment.."
            }
        }
        stage('deploy-stg') {
            steps {
                echo "Deployment of node application on STG environment.."
            }
        }
        stage('test-stg') {
            steps {
                echo "API test executuon against node application on STG environment.."
            }
        }
        stage('deploy-prd') {
            steps {
                echo "Deployment of node application on PRD environment.."
            }
        }
        stage('test-prd') {
            steps {
                echo "API test executuon against node application on PRD environment.."
            }
        }
    }
    
}
aqwq