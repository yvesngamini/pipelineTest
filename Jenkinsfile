pipeline {
    agent any
    tools {
       maven 'maven'
    }
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
              withMaven(traceability: true){
                      sh "mvn install"
                }
            }
        }
    }
}

