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
        parameters {
          string(name: 'PERSON', defaultValue: 'Kai', description: 'Who should I say hello to?')
        }
      }
      steps {
        sh 'hostname'
        sh 'node --version'
        echo "Hello, ${PERSON}, nice to meet you."
      }
    }
  }

  post {
    always {
      slackSend channel: '#jenkins-alerts', message: "Slack Message"
    }
  }
}