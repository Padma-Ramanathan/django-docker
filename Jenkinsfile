pipeline {

    agent any

    stages {
      stage(‘Build’) {
        steps {
          sh 'docker-compose up -d --build'
        }
      }
    }
     post {
      always {
          sh "docker-compose down || true"
      }
     }
}
