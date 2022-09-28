pipeline {
    agent {
        label {
            label 'built-in'
            customWorkspace '/mnt/projects/'
        }
    }
    stages {
        stage {
            steps {
                git clone https://github.com/tejasshete244/tejas-application.git -b 22Q2
            }
        }
        stage {
            steps {
                sh "scp -i /mnt/WINDOWSKEYPAIR.pem /mnt/projects/tejas-application/index.html ec2-user@172.31.36.227:/var/www/html/"
            }
        }
    }
    
}
