pipeline {
  agent any
  tools {
    nodejs 'node'
  }
  stages {
    stage('build') {
      steps {
        sh 'npm install'
      }
    }
    stage('test') {
      steps {
        sh 'npm test'
      }
    }
    stage('build') {
      steps {
        //just a sample
        sh 'npm --version'
      }
    }
  }
}