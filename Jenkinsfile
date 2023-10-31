pipeline {
    agent any
    withCredentials([string(credentialsId: 'SEMGREP_APP_TOKEN', variable: 'SEMGREP_APP_TOKEN')]) {
    }
    stages {
      stage('Semgrep-Scan') {
          steps {
            sh 'pip3 install semgrep'
            sh 'semgrep ci'
          }
      }
    }
  }
