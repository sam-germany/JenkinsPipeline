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
}