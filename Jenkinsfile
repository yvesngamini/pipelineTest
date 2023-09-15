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
                echo 'make a test1 '
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

