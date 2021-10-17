pipeline {
  agent any
  stages {
    stage('CI') {
      steps {
        echo 'Building'
      }
    }

    stage('DI') {
      steps {
        echo 'Testing'
      }
    }

  }
  post {
    always {
      echo 'Rodando!!!'
    }

    success {
      echo 'Sucesso!!!'
    }

    failure {
      echo 'Falha!!!'
    }

    unstable {
      echo 'Instavel!!!'
    }

    changed {
      echo 'Warning!!!'
    }

  }
}