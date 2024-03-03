pipeline {
    agent any 
    stages {
      
        stage("clone code") {
            steps {
                script {
                    // Let's clone the source
                    //git branch: 'main', credentialsId: 'github', url: 'https://github.com/vinayprakash893/docker-ec2-jenkins.git'
                      git branch: 'main', credentialsId: '70013610-30e4-4d1a-89a0-ff61e434be5c', url: 'https://github.com/nameismrudula/dockermysqlapp.git'
                }
            }
        }
        stage("build") {
            steps { 
                sh "docker build -t flask . "
            }
        }
        
        stage("deploy") {
          steps{
            sh "docker-compose down &&  docker-compose up -d "
          }
        }
      
    }
}

    


