pipeline {
    agent any

    stages {
        stage('GitClone') {
            steps {
                sh 'rm -rf prometheus-agent'
                sh 'git clone git@github.com:RadhikaBoga26/prometheus-agent.git'
                sh 'cd /var/lib/jenkins/workspace/pipe2/prometheus-agent'
                sh 'pwd'
                sh 'ls -al'
                
            }
        }
        stage('Packer image') {
            steps {
                echo 'Building image through packer..'
                sh 'packer build al2-build.json'

                
            }
        }
        
    }
}
