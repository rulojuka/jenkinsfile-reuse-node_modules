node(){
  def nodeHome = tool name: 'node-14-3-0', type: 'jenkins.plugins.nodejs.tools.NodeJSInstallation'
  env.PATH="${nodeHome}/bin:${env.PATH}"
  sh "echo $PATH"
  sh "node -v"
}
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh "npm run clean"
                sh "npm install"
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