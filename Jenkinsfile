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
        stage("Clone Repo") {
            steps {
                sh "git clone https://github.com/LeandroJ0se/Jenkins-Tests.git"
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
