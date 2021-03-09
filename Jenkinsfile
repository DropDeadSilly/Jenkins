pipeline {
  agent any

  environment {
    Abc = "Vasant Kumar"
  }

  stages {

    stage('Hello') {
      steps {
        sh 'echo ${Abc}!!!'
      }
    }

    stage('Like') {
      steps {
        sh 'hostname'
      }
    }
  }

  post {
    always {
      slackSend channel: '#jenkins-alerts', message: 'Cool, Slack messages working fine!'
    }
  }
}