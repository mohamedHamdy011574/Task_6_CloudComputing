pipeline {
    agent any

    stages {
        stage('Clone First Repo') {
            steps {
                // Clone the first repository where Jenkinsfile and bashfile.bat are located
                git url: 'https://github.com/mohamedHamdy011574/Task_6_CloudComputing.git'
            }
        }
        
        stage('Clone Second Repo') {
            steps {
                // Clone the second repository into a specific directory
                dir('second_repo') {
                    git url: 'https://github.com/mohamedHamdy011574/App_source_code_v5'
                }
            }
        }
        
        stage('Execute Script to Show Second Repo Contents') {
            steps {
                // Run the bashfile.bat located in the first repository and pass the path of the second repository
                bat 'bashfile.bat second_repo'
            }
        }
    }
}
