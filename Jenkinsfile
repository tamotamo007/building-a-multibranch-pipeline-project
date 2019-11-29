pipeline {
  parameters {
    choice(choices: ['dev', 'staging', 'production'], description: 'What stage?', name: 'stage')
    choice(choices: ['Build', 'Redeploy', 'Build and Redeploy'], description: 'What you wanna do?', name: 'action')
    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
    text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
    booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
    choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
    password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
  }
  agent {
    dockerfile {
      filename 'Dockerfile'
    }

  }
  stages {
    stage('Check') {
      steps {
        sh "echo ${params.region}"
      }
    }

  }
}
