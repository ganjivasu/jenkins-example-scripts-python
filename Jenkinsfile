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
        sh 'scp $workspace/hello.py ubuntu@34.209.11.56:~'
  }

    }
}
}
