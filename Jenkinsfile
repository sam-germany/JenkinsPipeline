pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'print build message'
          }
        }

        stage('Test') {
          steps {
            echo 'print Test step'
            echo '"Get the Key22 $(key22)"'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying the app --------'
      }
    }

  }
  environment {
    Key22 = 'abc_value'
  }
}