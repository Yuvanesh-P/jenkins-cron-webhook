pipeline{
    agent any

    triggers{
        cron('H/10 * * * *')
    }

    stages{
        stage('Checkout'){
            steps{
                echo 'Source code retrived from Github'
            }
        }
        stage('Install dependencies'){
            steps{
                bat 'python -m pip install -r requirements.txt'
            }
        }
        stage('Test'){
            steps{
                bat 'python -m pytest -v'
            }
        }
    }
} 