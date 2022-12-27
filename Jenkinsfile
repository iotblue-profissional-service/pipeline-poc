pipeline {
  agent any
  stages {
    stage('Static Analysis') {
      steps {
        sh '${scannerHome}/bin/sonar-scanner'
        input(message: 'Contimue to next step?', ok: 'yes')
        waitForQualityGate true
        office365ConnectorSend(webhookUrl: 'https://iotbluehq.webhook.office.com/webhookb2/3bdcf952-4e01-468a-a41b-b3f9500807a6@6e8fc0b9-cd4d-4388-98ce-6307800f0067/IncomingWebhook/5a6cc58153e94d3ba31424da37f907be/81eb40d5-4b67-44fb-82f8-4bcf23cbc288', message: 'SonarQube Results')
        waitUntil()
        input(message: 'Proceed to the next step?', ok: 'OK')
      }
    }

    stage('Unit Tests') {
      steps {
        echo 'Unit Tests Run'
      }
    }

  }
}