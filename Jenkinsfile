pipeline {
  agent {
    label 'SHELL'
  }
  stages {
    stage('Hello') {
      steps {
        sh 'echo Hi Vasant!!!'
        mail bcc: '', body: 'Test from Jenkins', cc: '', from: '', replyTo: '', subject: 'Test from Jenkins', to: 'kailesh5kumar@gmail.com'
      }
    }

  stage('Like') {
      steps {
        sh 'hostname'
        emailext body: 'Test from Jenkins', subject: 'Test from Jenkins', to: 'kailesh5kumar@gmail.com'
      }
    }
  }
}