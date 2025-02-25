// Jenkinsfile
pipeline {
    agent any
    parameters {
        string(name: 'Code_app', defaultValue: 'My-new-app')
        string(name: 'Commit_app', defaultValue: 'My-new-app')
        string(name: 'Build_app', defaultValue: 'My-new-app')
        string(name: 'Test_app', defaultValue: 'My-new-app')
        string(name: 'Review_app', defaultValue: 'My-new-app')
        string(name: 'Staging_app', defaultValue: 'My-new-app')
        string(name: 'Deploy_on_Prod_app', defaultValue: 'My-new-app')
        booleanParam(name: 'ExecuteTestAgain', defaultValue: '')
        booleanParam(name: 'Akshay', defaultValue: '')
        booleanParam(name: 'Rohan', defaultValue: '')
        choice(name: 'VERSION', choices: ['1.1', '1.2', '1.3', '1.4', '1.5'])
    }
    stages {
        stage('Code') {
            steps {
                script {
                    if (env.BRANCH_NAME == 'main') {
                        echo "Writing code for $Code_app "
                    }
                }
            }
        }
        stage('Commit') {
            steps {
                echo "Commiting code for $params.Commit_app"
            }
        }
        stage('Build') {
            steps {
                echo "Building code of $params.Build_app "
            }
        }
        stage('Test') {
            steps {
                echo "Testing of $params.Test_app "
            }
        }
        stage('Review') {
            steps {
                script {
                     if ( params.Akshay && params.Rohan == true ) {
                        echo "Both are reviewing $params.Review_app"
                     } else if ( params.Rohan == true) {
                        echo "Rohan is reviewing $params.Review_app"
                     } else if ( params.Akshay == true ) {
                        echo "Akshay is reviewing $params.Review_app"
                     } 
                     else {
                        echo "Jayesh is reviewing $params.Review_app"
                }
            }
        }
   }
        stage('TestAgain') {
            when {
                allOf{
                expression{ params.ExecuteTestAgain == true }
                }
            }
            steps {
                echo "Again testing of  $params.Staging_app"
            }
        }
        stage('Staging') {
            steps {
                echo "Staging of  $params.Staging_app"
            }
        }
        stage('Deploy on Production') {
            steps {
                echo "Deploying $params.Deploy_on_Prod_app  on Production Environment with version $params.VERSION"
            }
        }
    }
        post { 
            success { 
                echo "That's a successful build...!"
        }
    }
}
