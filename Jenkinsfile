pipeline {
  agent { docker { image 'node:16' } }
  stages {
    stage('Build') {
      steps {
        sh 'node --version'
        sh 'npm install --save'
      }
    }
  }
}
