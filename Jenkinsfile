pipeline {
  agent any
  stages {
    stage('example') {
      steps {
        withCredentials(bindings: [string(credentialsId: 'my-elastic-key', 
                                            variable: 'ELASTIC_ACCESS_KEY')]) {
          sh 'env | grep ELASTIC_ACCESS_KEY'
          sh "echo ${ELASTIC_ACCESS_KEY} > secret-file.txt"
        }

      }
    }

  }
}