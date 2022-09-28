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
                git clone https://github.com/tejasshete244/tejas-application.git
            }
        }
        stage {
            steps {
                sh "scp -i /mnt/WINDOWSKEYPAIR.pem /mnt/projects/tejas-application/index.html ec2-user@172.31.32.238:/var/www/html/"
            }
        }
    }
    
}
