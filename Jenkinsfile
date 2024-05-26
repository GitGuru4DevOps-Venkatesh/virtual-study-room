pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/GitGuru4DevOps-Venkatesh/virtual-study-room.git'
      }
    }
    stage('Build') {
      steps {
        sh 'cd frontend && docker build -t venkateshdocker1/frontend .'
        sh 'cd backend && docker build -t venkateshdocker1/backend .'
      }
    }
    stage('Test') {
      steps {
        // Add your test steps here
      }
    }
    stage('Deploy') {
      steps {
        sh 'kubectl apply -f deployment.yaml'
        sh 'kubectl apply -f service.yaml'
      }
    }
  }
}

