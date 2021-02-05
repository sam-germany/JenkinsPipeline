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
          environment {
            LocalVariable22 = 'Hello Local22'
          }
          steps {
            writeFile(file: 'LogTestFile22.txt', text: "This is an automation file  ${Key22} and localVariable ${LocalVariable22}")
          }
        }

      }
    }

    stage('Deploy') {
      when {
        branch 'main'
      }
      parallel {      
        stage('Deploy') {
          steps {
            input(message: 'Do you want to deploy -???--', id: 'OK')
            echo 'Deploying the app -------4444-'
          }
        }

        stage('Artifacts') {
          steps {
            archiveArtifacts 'LogTestFile22.txt'
         }
        }

      }
    }

  }
  environment {
    Key22 = 'abc_value'
  }
}

