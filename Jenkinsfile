pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        withAWS(credentials: 'aws-static', region:'us-west-2') {
          sh 'echo "Uploading to AWS"'
          s3Upload(file: 'index.html', bucket: 'static-website-pipeline')
        }
      }
    }
  }
}