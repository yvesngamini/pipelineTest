pipeline {
    agent any
    triggers{
        pollSCM '* * * * *'
    }
    stages {
        stage('Build') {
            steps {
                echo 'make a test '
            }
        }
        stage('test') {
            steps {
                bat mvn clean install pom.xml
            }
        }
    }
}

