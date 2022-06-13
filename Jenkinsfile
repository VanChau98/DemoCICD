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
                withDockerRegistry(credentialsId: 'docker-hub', url: 'https://index.docker.io/v1/') {
                    sh 'docker build -t VanChau98/DemoCICD:v2 .'
                    sh 'docker push VanChau98/DemoCICD'
                }
            }
        }
    }
}