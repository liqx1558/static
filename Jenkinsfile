pipeline {
  agent any
  stages {
    stage('Lint HTML') {
      steps {
        sh 'tidy -q -e *.html'
      }
    }
    stage('Upload To S3') {
      steps {
        withAWS(credentials: 'owread') {
          s3Upload(bucket: 'qixintest', file: 'index.html')
        }

      }
    }
  }
}