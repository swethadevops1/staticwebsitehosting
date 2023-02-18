pipeline {
    agent any 
    stages {
        stage('downloading and starting http server') { 
            steps {
                sh "sudo yum -y install httpd"
                sh "sudo systemctl start httpd"
            }
        }
        stage('cleaning existing www directory') { 
            steps {
                sh "sudo rm -rf /var/www/"
            }
        }
        stage('Git cloning') { 
            steps {
                sh "sudo git clone https://github.com/swethadevops1/staticwebsitehosting.git /var/www/html" 
            }
        }
    }
}
