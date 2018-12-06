pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'npm ci'
        sh 'npm run build'
      }

      post {
        success {
          echo "Now Archiving..."
          archiveArtifacts artifacts: '**/public/*'
        }
      }
    }
  }
}