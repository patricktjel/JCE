pipeline {
  agent any
  stages {
    stage('test') {
      steps {
        sh """
                                                        echo "Service user is $SERVICE_CREDS_USR"
                                                        echo "Service password is $SERVICE_CREDS_PSW"
                                                    """
      }
    }

  }
  environment {
    SERVICE_CREDS = credentials('git')
  }
}