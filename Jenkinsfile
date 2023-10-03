pipeline {
    agent any
    options {
        ansiColor('xterm')
    }
    stages {
        stage("Clean up") {
            steps {
                deleteDir()
            }
        }
        stage("Build") {
            steps {
                dir("Jenkins-Tests") {
                    sh "mvn clean install"
                }
            }
        }
        stage("Test") {
            steps {
                dir("Jenkins-Tests") {
                    sh "mvn test"
                }
            }
        }
    }
}
