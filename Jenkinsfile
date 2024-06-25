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
        //sh 'ssh-keyscan -H 34.209.11.56 >> ~/.ssh/known_hosts'
        sh 'scp $workspace/hello.py ubuntu@34.209.11.56:~'
  }

    }
}
}
