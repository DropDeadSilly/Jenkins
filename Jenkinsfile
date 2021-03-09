pipeline {
  agent any

  tools {
    nodejs 'nodejs-15'
  }

  stages {

    stage('Tool') {
      steps {
      input {
        message "Should we continue?"
        ok "Yes, we should."
        submitter "admin"
      }
        sh 'hostname'
        sh 'node --version'
      }
    }
  }

  post {
    always {
      slackSend channel: '#jenkins-alerts', message: "Slack Message"
    }
  }
}