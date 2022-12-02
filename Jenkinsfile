pipeline {
    agent ("krishna")
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
                sudo usermod -aG docker ubuntu
                systemctl restart docker
                docker info"""

            }
        }
    }
}