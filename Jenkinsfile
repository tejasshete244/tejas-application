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
                sh "rm -rf *"
                sh "git clone https://github.com/tejasshete244/tejas-application.git -b 22Q1"
            }
        }
        stage ('deploy'){
            steps {
                sh "scp -i /mnt/WINDOWSKEYPAIR.pem /mnt/projects/tejas-application/index.html ec2-user@172.31.32.238:/var/www/html/"
            }
        }
    }
    
}
