pipeline {
    agent any
    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/Sri-Udaya/jasperserver-sample-webapp.git'
            }
        }
        stage('build WAR') {
            environment {
                 mvnHome = tool 'maven3'
            }
            steps {
                sh "${env.mvnHome}/bin/mvn package"
             }
        }
    }
}
