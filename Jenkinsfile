pipeline {
    agent { 
        docker { 
            image 'node:14-alpine' 
        } 
    }

    stages {
        stage('clone repo') {
            steps {
                git branch: 'master',
                credentialsId: 'github-tombo',
                url: 'https://github.com/sdcilsy/todo-react.git'
            }
        }
        stage('build app') {
            steps {
                npm --version
            }
        }
    }
}