pipeline {

  agent {
    label 'master' // Útil para filtrar el tipo de agente
  }

  options {
    ansiColor('xterm')
    buildDiscarder(logRotator(numToKeepStr: '100'))
    disableConcurrentBuilds()
    timeout(time: 2, unit: 'HOURS')
    timestamps()
  }

  stages {
    stage('Hello world') {
      steps {
        echo 'Hello world!'
      }
    }
  }

  post {
    cleanup {
      cleanWs()
    }
  }
}
