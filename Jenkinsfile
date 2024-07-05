pipeline {
    agent any
    stages {
        
        stage("build"){
            steps{
                sh "sudo npm cache clean"
                sh "npm install"
                sh "npm run"
                echo 'Code build done'
            }
        }
        stage("deploy"){
            steps{
                sh "sudo rm -rf /var/www/react"
                sh 'sudo cp -r ${WORKSPACE}/build/ /var/www/react'
            }
        }
    }
}