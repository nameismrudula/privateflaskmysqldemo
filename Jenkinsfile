pipeline {
    agent any 
    stages {
      
        stage("clone code") {
            steps {
                script {
                    // Let's clone the source
                    //git branch: 'main', credentialsId: 'github', url: 'https://github.com/vinayprakash893/docker-ec2-jenkins.git'
                    // git branch: 'main', credentialsId: '70013610-30e4-4d1a-89a0-ff61e434be5c', url: 'https://github.com/nameismrudula/dockermysqlapp.git'
                       git branch: 'main', credentialsId: '70013610-30e4-4d1a-89a0-ff61e434be5c', url: 'https://github.com/nameismrudula/privateflaskmysqldemo'
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
            
             // sh "docker-compose -f docker-compose.yml -f docker-compose1.yml down -d"// && docker-compose -f docker-compose.yml -f docker-compose1.yml up"
              //sh "docker-compose -f docker-compose.yml -f docker-compose1.yml up -d "
              sh "docker-compose -f docker-compose.yml -f docker-compose1.yml down && docker-compose -f docker-compose.yml -f docker-compose1.yml up "

          }
        }
      
    }
}

    


