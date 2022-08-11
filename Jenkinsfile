pipeline {
    agent {
        kubernetes {
            cloud 'kubernetes'
      }
    }


    stages {
        stage('ls') {
            steps {
                sh 'ls'
            }
        }
        stage('date') {
            steps {
                container('default') {
                    sh 'date'
                }
            }
        }
//         stage('check version') {
//             steps {
//                 container('composer') {
//                     sh 'date'
//                 }
//             }
//         }
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
