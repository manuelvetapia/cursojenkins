pipeline {
  agent any
  stages {
    stage('Saludos') {
      steps {
        echo 'Hola mundo'
        sh '''printenv
echo $NOMBRE
mkdir nuevo
ls'''
      }
    }

    stage('Despedida') {
      steps {
        writeFile(file: 'holamundo.txt', text: 'adios $NOMBRE')
        archiveArtifacts(allowEmptyArchive: true, artifacts: '*.txt')
      }
    }

  }
  environment {
    NOMBRE = 'Manuel'
  }
}