pipeline {
  agent any
    stages {
      stage(’Build’) {
        steps {
          npm install
          npm install grunt-cli
          ./node_modules/grunt-cli/bin/grunt
        }
      }
    }
  post {
    always {
      archiveArtifacts artifacts: ’path/to/*.jar’,
      fingerprint: true
    }
  }
  }
