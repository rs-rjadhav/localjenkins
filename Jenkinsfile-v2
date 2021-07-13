pipeline {
    agent any
    parameters {
        string(name: 'Build_content', defaultValue:  'Building the app for the first time')
        string(name: 'Test_content', defaultValue: 'Testing the app for the first time')
        string(name: 'Deploy_DEV_content', defaultValue: 'Deploying the app for the first time on Dev Env')
        string(name: 'Testing_again_content', defaultValue: 'Testing the app for the second time')
        string(name: 'Deploy_PROD_content', defaultValue: 'Deploying the app for the first time on Prod Env')
    }
    stages {
        stage ('Build') {
            steps {
                echo "${params.Build_content}"
            }
        }
        stage ('Test') {
            steps {
                echo "${params.Test_content}"
            }
        }
        stage ('Deploy on Developement Environment') {
            steps {
                echo "${params.Deploy_DEV_content}"
            }
        }
        stage ('Testing again') {
            steps {
                echo "${params.Testing_again_content}"
            }
        }
        stage ('Deploy on Production Environment') {
            steps {
                echo "${params.Deploy_PROD_content}"
            }
        }
    }
}
