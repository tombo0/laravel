pipeline {
    agent {
      kubernetes {
        yaml '''
        apiVersion: v1
        kind: Pod
        metadata:
          labels:
            label: testing
        spec:
          containers:
          - name: composer
            image: composer
        '''

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
                    sh 'composer -v'
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
