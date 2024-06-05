pipeline {
    agent any
    stages{
        stage('build project'){
            steps{
                git url:'https://github.com/Chandu1998/Project-1-FinanceMe/', branch: "master"
                sh 'mvn clean package'
              
            }
        }
        stage('Build docker image'){
            steps{
                script{
                    sh 'docker build -t ckvk18/staragileprojectfinance:v1 .'
                    sh 'docker images'
                }
            }
        }
         
        
     stage('Deploy') {
            steps {
                sh 'sudo docker run -itd --name My-first-containe21211 -p 8083:8081 ckvk18/staragileprojectfinance:v1'
                  
                }
            }
        
    }
}
