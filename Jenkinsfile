pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'g++ -c PES1UG20CS542.cpp'
                sh 'g++ -o PES1UG20CS542 PES1UG20CS542.cpp'
                echo 'build stage successfull'
            }
        }
        stage('Test'){
            steps{
                sh './PES1UG20CS542'
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
