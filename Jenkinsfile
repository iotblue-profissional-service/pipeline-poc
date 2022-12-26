pipeline {
  agent any
  stages {
    stage('Static Analysis') {
      steps {
        sh '${scannerHome}/bin/sonar-scanner'
      }
    }

    stage('Unit Tests') {
      steps {
        echo 'Unit Tests Run'
      }
    }

  }
  environment {
    StaticCodeAnalysis = '1'
  }
}