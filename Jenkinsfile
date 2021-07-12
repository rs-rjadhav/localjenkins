pipeline {
    agent any
    stages {
        stage ("Build") {
            steps {
                echo 'Building the app for the first time'
            }
        }
        stage("Test") {
            steps {
                echo 'Testing the app for the first time'
            }
        }
        stage("Deploy on Developement Environment") {
            steps {
                echo 'Deploying the app for the first time on Developement Environment'
            }
        }
        stage("Testing again") {
            steps {
                echo 'Testing the app for the second time'
            }
        }
        stage("Deploy on Production Environment") {
            steps {
                echo 'Deploying the app for the first time on Production Environment'
            }
        }
    }
}
