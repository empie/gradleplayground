pipeline {
  agent any
  stages {
    stage('test') {
      steps {
        echo 'test'
      }
    }
    stage('pull') {
      steps {
        parallel(
          "pull": {
            retry(count: 10) {
              error 'Failed'
            }
            
            
          },
          "": {
            waitUntil() {
              dir(path: '/opt/')
            }
            
            
          }
        )
      }
    }
  }
}