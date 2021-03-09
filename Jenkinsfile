pipeline {
  agent any

  tools {
    nodejs 'nodejs-15'
  }

  stages {

    stage('Tool') {
      input {
        message "Should we continue?"
        ok "Yes, we should."
        submitter "admin"
      }
      steps {
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