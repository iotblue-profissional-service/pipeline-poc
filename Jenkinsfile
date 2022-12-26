pipeline {
  agent any
  stages {
    stage('Static Analysis') {
      steps {
        sh '${scannerHome}/bin/sonar-scanner'
        input(message: 'Contimue to next step?', ok: 'yes')
      }
    }

    stage('Unit Tests') {
      steps {
        echo 'Unit Tests Run'
      }
    }

  }
}