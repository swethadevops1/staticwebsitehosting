pipeline {
    agent { label 'slave2' }
    stages {
        stage('downloading && starting http server') { 
            steps {
                sh "sudo yum -y install httpd"
                sh "sudo systemctl start httpd"
            }
        }
        stage('cloning project') { 
            steps {
                sh "sudo git clone https://github.com/swethadevops1/staticwebsitehosting.git /var/www/html"
            }
        }
    }
