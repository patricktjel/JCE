pipeline {
  agent any
  stages {
    stage('example') {
      when {
        equals expected: 'Patrick', actual: "${PERSON}"
      }
      input {
        message 'Should we continue?'
        id 'Yes'
        parameters {
          string(name: 'PERSON', defaultValue: 'Mr', description: 'Who?')
        }
      }
      steps {
        echo 'test'
      }
    }

  }
}