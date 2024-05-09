pipeline {
    agent any
    
    stages {
        stage('removing old data') {
            steps {
             
                   sh 'sudo rm -rf /var/www/html'
                   }
                 }

  stage('remove old software') {
         steps {
              sh 'sudo  yum remove httpd -y '
                 }
     }
                 
        stage('installin software') {
            steps {
                sh 'sudo yum install httpd -y'
                }
              }
              
        stage('start service') {
            steps {
                
                   sh  'sudo systemctl start httpd'

                  }
                }
                
        stage('coping webpage') {
            steps {
                sh 'sudo git clone https://github.com/ashwindevop/myweb1may.git  /var/www/html'

            }
        }
    }    
}

