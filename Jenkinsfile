pipeline {
    agent { 
        docker { 
            image 'node' 
        } 
    }

    stages {
        stage('ls') {
            steps {
                sh 'ls'
            }
        }
        stage('clone repo') {
            steps {
                git branch: 'master',
                credentialsId: 'github-tombo',
                url: 'https://github.com/sdcilsy/todo-react.git'
            }
        }
        stage('build app') {
            steps {
                sh 'npm install'
            }
        }
        stage ('test app') {
            steps {
                sh 'npm test'
            }
        }
        stage ('deploy app') {
            steps {
                sh 'npm start'
            }
        }
    }
}