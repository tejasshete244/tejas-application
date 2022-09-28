pipeline {
    agent {
        label {
            label 'built-in'
            customWorkspace '/mnt/projects/'
        }
    }
    stages {
        stage ('git clone'){
            steps {
                sh "git clone https://github.com/tejasshete244/tejas-application.git"
            }
        }
        stage ('deploy'){
            steps {
                sh "scp -i /mnt/WINDOWSKEYPAIR.pem /mnt/projects/tejas-application/index.html ec2-user@172.31.36.227:/var/www/html/"
            }
        }
    }
    
}
