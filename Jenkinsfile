pipeline {
  agent any
  stages {
    stage('FetchCode') {
      steps {
        echo 'Code From GitHub'
      }
    }
    stage('Bundling') {
      parallel {
        stage('Compile') {
          steps {
            echo 'Compiling Java Code'
          }
        }
        stage('Javac') {
          steps {
            echo 'javac Execution'
          }
        }
        stage('Command') {
          steps {
            bat 'javac EmpMain.java'
          }
        }
      }
    }
    stage('Testing') {
      steps {
        echo 'Testing Completed'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deployed in Server'
      }
    }
  }
}