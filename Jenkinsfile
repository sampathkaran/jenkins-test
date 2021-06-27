pipeline {
  agent any
  stages {
    stage('test') {
      steps {
        echo 'this is build of $BUILD_NUMBER by $DEMO '
        sh 'echo "this is my $BUILD_NUMBER of MR $DEMO"'
      }
    }

  }
  environment {
    DEMO = 'don'
  }
}