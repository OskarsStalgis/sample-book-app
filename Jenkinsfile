pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                build()
            }
        }
        stage('deploy-dev') {
            steps {
                deploy("DEV")
            }
        }
        stage('test-dev') {
            steps {
                test("DEV")
            }
        }
        stage('deploy-stg') {
            steps {
               deploy("STG")
            }
        }
        stage('test-stg') {
            steps {
                test("STG")
            }
        }
        stage('deploy-prd') {
            steps {
                deploy("PRD")
            }
        }
        stage('test-prd') {
            steps {
                test("PRD")
            }
        }
    }
    
}

def build(){
    echo "Building of node application is starting.."
}

def deploy(String environment){
    echo "Deployment of node application on ${enviroment} environment.."
}

def test(String enviroment){
    echo "API test executuon against node application on ${enviroment} environment.."
}
