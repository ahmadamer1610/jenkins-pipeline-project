pipeline {
    agent {
        label "jenkins-agent"
    }
    tools {
        jdk "Java17"
        maven "Maven3"
    }
    stages {
        stage("cleanup workspace") {
            steps {
                cleanWs()
            }
        }

        stage("Checkout from SCM") {
            steps {
                git branch: 'main', credentialsId: 'jenkins-2', url: 'https://github.com/ahmadamer1610/jenkins-pipeline-project/blob/main/Jenkinsfile:'
            }
        }
    }
}
