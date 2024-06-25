pipeline {
  agent any
  stages {
    stage('version') {
      steps {
        sh 'python3 --version'
      }
    }
    stage('hello') {
      steps {
        sh 'python3 hello.py'
      }
    }
    stage("copy to server") {
      steps {
        script {
        sshagent(credentials: ['ubuntu']) {
        //sh 'ssh-keyscan -H 34.209.11.56 >> ~/.ssh/known_hosts'
        sh 'ssh -o StrictHostKeyChecking=no scp hello.py ubuntu@34.209.11.56:~'
        }
        }
      }
    }
}
}
