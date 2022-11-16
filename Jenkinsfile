pipeline {
  agent any
  stages {
    stage('test') {
      steps {
        echo 'tmp'
        timeout(time: 3, unit: 'SECONDS') {
          input(message: 'Deploy to Stage', ok: 'Yes, let\'s do it!')
        }

      }
    }

  }
}