pipeline {
  agent any
  stages {
    stage('Check for merge conflicts') {
      steps {
        echo '"Running merge conflict check"'
      }
    }
    stage('Run unit tests') {
      steps {
        echo '"Executing PegaUnit test suite"'
      }
    }
    stage('Merge branch') {
      steps {
        echo '"Merging Branch"'
      }
    }
  }
}