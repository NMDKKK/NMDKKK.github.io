pipeline {
  agent any
  stages {
    stage('Log Tool Version') {
      steps {
        sh '''mvn --version
java --version'''
      }
    }

    stage('Build with maven') {
      steps {
        sh 'mvn compile test package'
      }
    }

    stage('Post Build Steps') {
      steps {
        writeFile(file: 'status.txt', text: 'hey ken!!')
      }
    }

  }
}