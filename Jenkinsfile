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
        sh 'npm run coverage'
      }
      post {
        always {
        publishHTML target: [
          allowMissing         : false,
          alwaysLinkToLastBuild: false,
          keepAll             : true,
          reportDir            : 'coverage',
          reportFiles          : 'index.html',
          reportName           : 'Code Coverage'
        ]
        }
      }
    }
    stage('deploy') {
      steps {
        //just a sample
        sh 'npm --version'
      }
    }
  }
}