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
        stage('Current dir') {
          steps {
            sh '''



echo $PWD
ls -l'''
          }
        }
      }
    }
    stage('Random') {
      steps {
        sh 'echo $RANDOM'
      }
    }
    stage('Checkout') {
      parallel {
        stage('Checkout') {
          steps {
            git(url: 'https://github.com/RS-X/jenkinsfun.git', branch: 'master')
          }
        }
        stage('ntscout') {
          steps {
            git(url: 'https://github.com/bad-trip/NTScout.git', branch: 'master')
          }
        }
      }
    }
    stage('Find') {
      steps {
        sh 'find'
      }
    }
  }
}