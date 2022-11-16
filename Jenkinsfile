pipeline {
  agent any
  stages {
    stage('test') {
      steps {
        sh 'echo abcd > test.txt'
        archiveArtifacts(artifacts: 'test.txt', fingerprint: true)
      }
    }

  }
}