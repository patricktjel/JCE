pipeline {
  agent any
  stages {
    stage('parallel') {
      failFast true
      parallel {
        stage('Buzz Build') {
          agent any
          steps {
            echo "The value is: ${TEST}"
            sh './test.sh'
          }
        }

        stage('failfast') {
          steps {
            echo 'parallel'
            sleep 5
          }
        }

      }
    }

  }
  environment {
    TEST = 'test'
  }
}