pipeline {
    agent { label "dev-server"}
    
    stages {
        
        stage("build"){
            steps{
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