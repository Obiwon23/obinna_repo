pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/Obiwon23/obinna_repo.git'
      }
    }

    stage('Build') {
      steps {
        sh 'mvn clean install'
      }
    }

    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }

    stage('Archive Artifacts') {
      steps {
        archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
      }
    }
  }

  post {
    always {
      echo 'Pipeline finished.'
    }
    success {
      echo 'Build succeeded!'
    }
    failure {
      echo 'Build failed.'
    }
  }
}
