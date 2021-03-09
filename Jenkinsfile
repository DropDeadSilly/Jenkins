pipeline {
  agent any

  tools {
    nodejs 'nodejs-15'
  }

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