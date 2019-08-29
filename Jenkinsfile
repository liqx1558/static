pipeline {
  agent any
  stages {
    stage('') {
      steps {
        withAWS(credentials: 'owread') {
          s3Upload(bucket: 'qixintest', file: 'index.html')
        }

      }
    }
  }
}