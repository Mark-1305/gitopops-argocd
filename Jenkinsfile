pipeline {
  agent any

  environment {
    DOCKERHUB_USERNAME = "manoharshetty507"
    APP_NAME = "gitops-argo-app"
    IMAGE_TAG = "${BUILD_NUMBER}"
    IMAGE_NAME = "${DOCKERHUB_USERNAME}/${APP_NAME}"
    REGISTRY_CREDS = "dockerhub"
  }

  stages {
    stage('Cleanup workspace') {
      steps {
        script {
          cleanWs()
        }
      }
    }

    stage('Checkout SCM') {
      steps {
        script {
          git branch: 'main',
          url: 'https://github.com/Mark-1305/gitopops-argocd.git'
        }
      }
    }

    stage('Build Docker image') {
      steps {
        script {
          docker_image = docker.build("${IMAGE_NAME}:${IMAGE_TAG}")
        }
      }
    }

    // Add additional stages if necessary
  }
}
