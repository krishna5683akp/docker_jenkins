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
                sh "docker info"
            }
        }
    }
}