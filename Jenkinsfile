pipeline{
    agent any

    stages{
        stage('git checkout'){
            steps{
                git branch : 'main' , url :'https://github.com/ShijithDG/Jenkins-Test.git'
            }
        }
        stage('Run script'){
            steps{
                sh 'python3 number.py'
            }
        }
    }
    post{
        always{
            echo 'cleaning'
        }
        failure{
            echo 'failed'
        }
        success{
            echo 'success'
        }
    }
}