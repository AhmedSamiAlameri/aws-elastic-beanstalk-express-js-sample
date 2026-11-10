pipeline {
  agent { docker { image 'node:16' } }
  stages {
    stage('Build') {
      steps {
        sh 'node --version'
        sh 'npm install --save'
      }
    }
    stage('Scan') {
      steps {
        // Report dependency vulnerabilities. Non-blocking: the upstream sample app
        // pins older transitive deps (proxy-addr, qs); findings are logged for review.
        sh 'npm audit || true'
      }
    }
  }
}
