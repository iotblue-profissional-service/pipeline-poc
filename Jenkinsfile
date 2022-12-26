pipeline {
  agent any
  stages {
    stage('Static Analysis') {
      steps {
        sh '${scannerHome}/bin/sonar-scanner'
      }
    }

  }
  environment {
    StaticCodeAnalysis = '1'
  }
}