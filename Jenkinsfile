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

        stage("Build Application") {
            steps {
                sh 'mvn clean package'
               }
        }
        stage("Test Application") {
            steps {
                               sh 'mvn test'

            }
        }
    }
}
