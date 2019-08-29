pipeline {
  agent any
  stages {
    stage('Lint HTML') {
      steps {
        sh 'tidy -q -e *.html'
        withAWS(credentials: 'owread') {
          s3Upload(bucket: 'qixintest', file: 'index.html')
        }

      }
    }
  }
}