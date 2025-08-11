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
        echo 'Running build steps...'
        sh 'echo "Build successful!"'
        echo 'Application built'
      }
    }

    stage('Test') {
      steps {
        echo 'Running tests...'
        sh 'echo "All tests passed!"'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying application...'
        sh 'echo "Deployment complete!"'
      }
    }
  }

  post {
    success {
      echo 'Pipeline completed successfully.'
    }
    failure {
      echo 'Pipeline failed.'
    }
  }
}
