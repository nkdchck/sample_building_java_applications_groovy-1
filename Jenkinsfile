@Library('jenkins-shared-lib') _

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                checkout scm
                sh 'chmod +x gradlew'
                sh './gradlew build'
            }
        }
        stage('Shared Library Test') {
            steps {
                welcome("Rick Sanchez")
                script {
                    calculator.add(2, 2)
                    calculator.mul(3, 5)
                } 
            } 
        }
    }
}
