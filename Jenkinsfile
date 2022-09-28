pipeline {
    agent {
        label {
            label 'built-in'
            customWorkspace '/mnt/projects/3/'
        }
    }
    stages {
        stage ('git clone'){
            steps {
                sh "rm -rf *"
                sh "git clone https://github.com/tejasshete244/tejas-application.git -b 22Q3"
            }
        }
        stage ('deploy'){
            steps {
                sh "scp -i /mnt/WINDOWSKEYPAIR.pem /mnt/projects/3/tejas-application/index.html ec2-user@172.31.36.230:/var/www/html/"
            }
        }
    }
    
}
