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
        httpRequest(url: 'http://localhost:8080/prweb/PRRestService/PegaUnit/Rule-Test-Unit-Case/pzExecuteTests?AccessGroup=Designs:Administrators', consoleLogResponseBody: true, acceptType: 'NOT_SET', contentType: 'NOT_SET', httpMode: 'POST', ignoreSslErrors: true, responseHandle: 'STRING', authentication: 'PegaUnitTestAuth', outputFile: 'result.xml')
        junit '**/result.xml'
      }
    }
    stage('Merge branch') {
      steps {
        echo '"Merging Branch"'
      }
    }
  }
}