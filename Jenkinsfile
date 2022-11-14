pipeline {
  agent any
  stages {
    stage('Buzz Build') {
      agent any
      steps {
        echo "The value is: ${TEST}"
        sh './jenkins/build.sh'
        archiveArtifacts(artifacts: 'target/*.jar', fingerprint: true)
      }
    }

    stage('Buzz Test') {
      steps {
        sh './jenkins/test-all.sh'
      }
    }

    stage('error') {
      steps {
        junit '**/surefire-reports/**/*.xml'
      }
    }

  }
  environment {
    TEST = 'test'
  }
}