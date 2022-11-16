pipeline {
  agent any
  stages {
    stage('test') {
      steps {
        echo 'tmp'
        sleep 2
      }
    }

  }
  options {
    timeout(time: 1, unit: 'SECONDS')
  }
}