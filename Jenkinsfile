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

    stage('adicional') {
      steps {
        sh 'git remote -v'
      }
    }

  }
  environment {
    NOMBRE = 'Manuel'
  }
}