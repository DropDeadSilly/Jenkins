pipeline {
  agent any

  environment {
    Abc = "Vasant Kumar"
  }

  parameters {
    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

    text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

    booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

    choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

    password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
  }

  stages {

    stage('Hello') {
      steps {
        sh 'echo ${Abc}!!!'
        sh 'PERSON NAME :  ${PERSON}!!!'
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
      slackSend channel: '#jenkins-alerts', message: "Hi, ${Abc}!"
    }
  }
}