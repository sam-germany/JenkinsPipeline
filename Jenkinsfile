pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'printing method for my Java application'
          }
        }

        stage('Test') {
          steps {
            echo 'Testing the application'
            echo 'with the arguments $jfd-------k'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: 'do u want to deploy', id: 'ok')
        echo 'Deploying the app in IIS server'
      }
    }

  }
  environment {
    abc = 'aa'
  }
}