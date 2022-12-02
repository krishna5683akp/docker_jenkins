pipeline {
    agent { label 'krishna' }
    stages {
        stage ("git"){
            steps {
                git branch: "master", url: "https://github.com/krishna5683akp/docker_jenkins.git"
            }
        }
        stage ("sh") {
            steps {
                sh """sudo apt update
                curl -fsSL https://test.docker.com -o test-docker.sh
                sh test-docker.sh
                sudo systemctl start docker
                sudo systemctl enable docker
                sudo usermod -aG docker ubuntu
                sudo systemctl restart docker
                sudo docker info"""

            }
        }
    }
}