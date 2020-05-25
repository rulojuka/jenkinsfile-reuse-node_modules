pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh "npm run clean"
                echo 'Done building'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh "npm test"
                echo 'Done testing.'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                sh "npm run hello"
                echo 'Done deploying.'
            }
        }
    }
}