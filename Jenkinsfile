pipeline {

  agent any

  stages {

    stage('Clonar repositório') {

      steps {

        git branch: 'main', url: 'https://github.com/brunodsn/testes-api-cy.git'

      }

    }

    stage('Instalar dependencias') {

      steps {

        bat 'npm install'

      }

    }

    stage('Subir servidor') {

      steps {

        bat 'npm start'

      }

    }

    stage('Executar testes') {

      steps {

        bat 'NO_COLOR=1 npm run cy:run'

      }

    }

  }

}