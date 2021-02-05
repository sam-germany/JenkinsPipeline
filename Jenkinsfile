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
            echo "Get the Key22 ${Key22}"
          }
        }

        stage('Test Log') {
          steps {
            writeFile(file: 'LogTestFile22.txt', text: 'This is an automation file')
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Do you want to deploy ---', id: 'OK')
        echo 'Deploying the app -------4444-'
      }
    }

  }
  environment {
    Key22 = 'abc_value'
  }
}