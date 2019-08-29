pipeline {
  agent any
  stages {
    stage('Upload to S3') {
      steps {
        withAWS(credentials: 'owread') {
          s3Upload(bucket: 'qixintest', file: 'index.html')
        }

      }
    }
  }
}