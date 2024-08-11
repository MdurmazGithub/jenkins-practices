
pipeline {
    agent any // { label 'master' }

    options {
        timestamps ()
        ansiColor('vga')
        buildDiscarder(logRotator(numToKeepStr: '3'))
    }
    stages {
        stage('build') {
            steps {
                echo "Pipeline job with Jenkinsfile"
                sh 'echo using shell within Jenkinsfile'
                sh 'javac Hello.java'
//                 sh 'java Hello'
                echo 'not using shell in the Jenkinsfile'
            }
        }
        stage('run') {
            steps {
                echo "Pipeline job with Jenkinsfile"
                sh 'echo Running java file'
                sh 'java Hello'
                echo 'Java file run successfully!!!'
            }
        }
    }
}
