pipeline {
  agent any

  environment {
    ENV = 'qa'
  }

  stages {
    stage('First stage') {
      steps {
        echo 'qwerty'
        dir(path: 'jenkins') {
          echo 'asd'
        }
        load 'jenkins/lib.groovy'
        readTrusted 'jenkins/trusted.groovy'
        script {
          echo 'arbitrary script'
        }
      }
    }
  }

  post {
    always {
      cleanWs()
    }
  }
}
