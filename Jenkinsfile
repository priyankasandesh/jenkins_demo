pipeline {
    agent any
    environment {
            NODE_ENV= "Production"
    }
    stages {
        stage('Hello') {
            steps {
                git 'https://github.com/priyankasandesh/jenkins_demo.git'
                echo 'output from GIT'
                sh 'cat jenkins_git.txt'
            }
        }
        stage('Prod') {
            environment{
                NAME ='Priyanka'
            }
            steps {
                echo NODE_ENV
                echo NAME
            } 
        } 
        stage('artifacts') {
            steps {
                archiveArtifacts artifacts: '**', followSymlinks: false
            } 
        }    
    }
}