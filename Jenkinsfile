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
        stage('check version') {
            steps {
                container('composer') {
                    sh 'composer --version'
                }
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
