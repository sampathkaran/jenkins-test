pipeline {
  agent any
  stages {
    stage('test') {
      steps {
        echo 'echo " this is build of $BUILD_NUMBER by $DEMO "'
      }
    }

  }
  environment {
    DEMO = 'don'
  }
}