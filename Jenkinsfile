pipeline{
    agent any
    stages{
        stage('Clone stage'){
            steps{
                git 'https://github.com/VanChau98/DemoCICD.git'
            }
        }
        stage('Docker'){
            steps{
                withDockerRegistry(credentialsId: 'docker-hub demo', url: 'https://index.docker.io/v1/') {
                    sh 'docker build -t vanchau98/DemoCICD .'
                    sh 'docker push vanchau98/DemoCICD'
                }
            }
        }
    }
}