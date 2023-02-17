pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'g++ -c main/jenkinstest.cpp'
                sh 'g++ -o jenkinstest main/jenkinstest.cpp'
                echo 'build stage successfull'
            }
        }
        stage('Test'){
            steps{
                sh './jenkinstestu'
                echo 'Test successful'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deployment Successful'
            }
        }
    }
    post{
        failure{
            echo 'Pipeline Failed'
        }
    }
}
