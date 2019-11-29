pipeline {
  parameters {
    choice(choices: ['dev', 'staging', 'production'], description: 'What stage?', name: 'stage')
    choice(defaultValue: "Build and Redeploy",choices: ['Build', 'Redeploy', 'Build and Redeploy'], description: 'What you wanna do?', name: 'action')
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
