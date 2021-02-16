pipeline {
  agent any
  stages {
    stage('Saludos') {
      steps {
        echo 'Hola mundo'
        sh 'printenv'
      }
    }

    stage('Despedida') {
      steps {
        writeFile(file: 'holamundo.txt', text: 'adios')
        archiveArtifacts(allowEmptyArchive: true, artifacts: '*.txt')
      }
    }

  }
}