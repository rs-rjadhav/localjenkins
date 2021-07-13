// jenkinsfile-v3
pipeline {
    agent any
    parameters {
        string(name: 'Code_app', defaultValue:  'My-new-app')
        string(name: 'Commit_app', defaultValue: 'My-new-app')
        string(name: 'Build_app', defaultValue: 'My-new-app')
        string(name: 'Test_app', defaultValue: 'My-new-app')
        string(name: 'Review_app', defaultValue: 'My-new-app')
        string(name: 'Staging_app', defaultValue: 'My-new-app')
        string(name: 'Deploy_on_Prod_app', defaultValue: 'My-new-app')
        booleanParam(name: 'ExecuteTestAgain', defaultValue: true)
        choice(name: 'VERSION', choices ['1.1','1.2','1.3','1.4','1.5'])
    }
    stages {
        stage ('Code') {
            if (BRANCH_NAME) {
                BRANCH_NAME == 'main'
                }
            }
            steps {
                echo "Writing code for $Code_app "
            }
        }
        stage ('Commit') {
            steps {
                echo "Commiting code for $Commit_app "
            }
        }
        stage ('Build') {
            steps {
                echo "Building code of $Build_app "
            }
        }
        stage ('Test') {
            steps {
                echo "Testing of $Test_app "
            }
        }
        stage ('Review') {
            steps {
                echo "Reviewing $Review_app"
            }
        }
        stage ('TestAgain') {
            when {
                ExecuteTestAgain == true
            }
        }
        stage ('Staging') {
            steps {
                echo "Staging of  $Staging_app"
            }
        }
        stage ('Deploy on Production') {
            steps {
                echo "Deploying $Deploy_on_Prod_app  on Production Environment with version $params.VERSION"
            }
        }
    }
}
