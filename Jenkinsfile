pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                buildApp()
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

def buildApp(){
    echo "Building of node application is starting.."
    sh "docker build -t oskarsstalgis/sample-book-app ."

    echo "Pushing img to Docker registry.."
    sh "docker push oskarsstalgis/sample-book-app"
}

def deploy(String enviroment){
    echo "Deployment of node application on ${enviroment} environment.."
    sh "docker pull oskarsstalgis/sample-book-app"
    sh "docker compose stop sample-book-app-${enviroment.toLowerCase()}"
    sh "docker compose rm sample-book-app-${enviroment.toLowerCase()}"
    sh "docker compose up -d sample-book-app-${enviroment.toLowerCase()}"

}

def test(String enviroment){
    echo "API test executuon against node application on ${enviroment} environment.."
}
