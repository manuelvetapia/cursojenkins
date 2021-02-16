pipeline {
  agent any
  stages {
    stage('Saludos') {
      steps {
        echo 'Hola mundo'
        sh '''printenv
echo $NOMBRE
mkdir nuevo
ls
git status'''
      }
    }

    stage('Despedida') {
      steps {
        writeFile(file: 'holamundo.txt', text: 'adios ')
        archiveArtifacts(allowEmptyArchive: true, artifacts: '*.txt')
        sh '''ls
git status'''
      }
    }

  }
  environment {
    NOMBRE = 'Manuel'
  }
}