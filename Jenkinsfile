pipline {
    agent any
    stages {
        stage('init'){
            steps{
                sh 'docker stop nodejs-project || true'
                sh 'docker rm nodejs-project || true'
                
            }
        }
        stage('build images'){
            steps{
                sh 'docker build -t nodejs-project:${BUILD_NUMBER} .'
            }
        }
        stage('Run'){
            steps{
                sh 'docker run -d -p 80:5000 --name nodejs-project nodejs-project:${BUILD_NUMBER}'
            }
        }
    }




}
