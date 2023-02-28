pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'g++ -c PES1UG21CS808.cpp'
                sh 'g++ -o PES1UG21CS808 PES1UG21CS808.cpp'
                echo 'build stage successful'
            }
        }
        stage('Test'){
            steps{
                sh './PES1UG21CS808'
                echo 'Test stage executed successfully'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deployed Successfully'
            }
        }
    }
    post{
        failure{
            echo 'Pipeline Failed'
        }
    }
}
