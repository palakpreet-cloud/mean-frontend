pipeline{
    agent any
    tools{
        nodejs 'mynode'
    }
    stages{
        stage('git'){
            steps{
                git url: 'https://github.com/palakpreet-cloud/mean-frontend.git', branch: 'main'
            }
        }
        stage('build'){
            steps{
                sh 'docker build -t frontend .'
            }
        }
        stage('start'){
            steps{
                sh 'docker run -d -p 4200:4200 --name frontend frontend'
            }
        }
    }
}