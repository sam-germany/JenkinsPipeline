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
            echo 'with the arguments $jfdk'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying the app in IIS server'
      }
    }

  }
  environment {
    abc = 'aa'
  }
}