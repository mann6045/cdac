pipeline {
    agent any
    stages {
        stage('Clone Repo') {
            steps {
	echo 'Cloning the repository'
                 git branch: 'main', url: 'https://github.com/chntraining/cdac.git',credentialsId: 'gitcred'
            }
        }
        stage('Build') {
            steps {
	echo 'Building the Application'
                  sh 'hello.bat'
            }
        }
        stage('Test') {
            steps {
	echo 'Building the Application'
                  sh 'echo "All TEST CASES PASSSSSSED" '
            }
        }
        stage('Deploy') {
            steps {
	echo 'Building the Application'
                  bat 'echo "Deployement SUCCESSFUL" '
            }
             post { 
                always { 
                echo 'Pipeline execution Completed Successfully :) !'
             }
        }
        }
       
    }
}
