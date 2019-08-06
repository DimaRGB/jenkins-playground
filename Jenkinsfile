pipeline {
  agent any
  stages {
    stage('First stage') {
      steps {
        echo 'qwerty'
        dir(path: 'jenkins') {
          echo 'asd'
        }

        cleanWs(cleanWhenSuccess: true, cleanupMatrixParent: true)
        load 'jenkins/lib.groovy'
        readTrusted 'jenkins/trusted.groovy'
        deleteDir()
        script {
          echo 'arbitrary script'
        }

      }
    }
  }
  environment {
    ENV = 'qa'
  }
}