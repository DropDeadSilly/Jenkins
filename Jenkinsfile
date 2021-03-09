pipeline {
  agent any

  stages {

    stage('Tool') {
      steps {
        sh 'hostname'
      }
    }
  }

  post {
    always {
      slackSend channel: '#jenkins-alerts', message: "Slack Message"
    }
  }
}