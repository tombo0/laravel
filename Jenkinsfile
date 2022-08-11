pipeline {
    agent { 
        any { 
            image 'composer' 
        } 
    }

    stages {
        stage('ls') {
            steps {
                sh 'ls'
            }
        }
        stage('check version') {
            steps {
                sh 'php --version'
            }
        }
//         stage('build app') {
//             steps {
//                 sh 'php install'
//             }
//         }
//         stage ('test app') {
//             steps {
//                 sh 'npm test'
//             }
//         }
//         stage ('deploy app') {
//             steps {
//                 sh 'npm start'
//             }
//         }
    }
}
