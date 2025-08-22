@Library('shared-library') _

pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    myLibrary.hello()
                }
                sh 'mvn clean package'
            }
        }
        stage('Run') {
            steps {
                sh 'java -jar target/minimal-app-1.0-SNAPSHOT.jar'
            }
        }
    }
}
