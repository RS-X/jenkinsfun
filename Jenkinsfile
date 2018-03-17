pipeline {
  agent any
  stages {
    stage('Hello') {
      parallel {
        stage('Hello') {
          steps {
            sleep 2
            echo 'Hello World'
          }
        }
        stage('World') {
          steps {
            echo 'World'
            sleep 5
          }
        }
      }
    }
    stage('Random') {
      steps {
        sh 'echo $RANDOM'
      }
    }
  }
}