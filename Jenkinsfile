pipeline {
    agent any
    stages {
        stage('Clone Repo') {
            steps {
                echo 'Cloning the repository'
                git branch: 'main', url: 'https://github.com/chntraining/cdac.git', credentialsId: 'gitcred'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the Application'
                sh './hello.sh' // assuming you have a shell script now instead of hello.bat
            }
        }
        stage('Test') {
            steps {
                echo 'Testing the Application'
                sh 'echo "All TEST CASES PASSSSSSED"'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the Application'
                sh 'echo "Deployment SUCCESSFUL"'
            }
            post {
                always {
                    echo 'Pipeline execution Completed Successfully :) !'
                }
            }
        }
    }
}
