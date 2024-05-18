pipeline {
    agent any

    stages {
        stage('Clone First Repo') {
            steps {
                // Clone the first repository where Jenkinsfile is located
                git url: 'https://github.com/mohamedHamdy011574/Task_6_CloudComputing.git'
            }
        }
        
        stage('Clone Second Repo and Execute Script') {
            steps {
                // Clone the second repository
                dir('second_repo') {
                    git url: 'https://github.com/mohamedHamdy011574/App_source_code_v5'
                }
                
                // Execute the bashfile.bat located in the second repo
                dir('second_repo') {
                    bat 'https://github.com/mohamedHamdy011574/Task_6_CloudComputing/blob/master/bashfile.bat'
                }
            }
        }
    }
}
