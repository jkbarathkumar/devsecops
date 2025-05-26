@Library('my-maven@main') _

pipeline {
    agent any 

    environment {
        DOCKER_CREDENTIALS_ID = 'docker-hub-credentials'
    }

    stages {
        stage("Git Checkout") {
            steps {
                git branch: 'main', changelog: false, poll: false, url: 'https://github.com/jkbarathkumar/devsecops'
            }
        }

        stage("Compile") {
            steps {
                mavenBuild()
            }
        }
    }
}


        
       

    
