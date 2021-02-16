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
        sh '''ls
git remote -v
git add holamundo.txt
git push origin main'''
      }
    }

  }
  environment {
    NOMBRE = 'Manuel'
  }
}