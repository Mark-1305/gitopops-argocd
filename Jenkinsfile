pipeline {
  agent any

  enviroment{
    DOCKERHUB_USERNAME = "manoharshetty507"
    APP_NAME = "gitops-argo-app"
    IMAGE_TAG = "${BUILD_NUMBER} 
    IMAGE_NAME = "${DOCKERHUB_USERNAME}" + "/" + "${APP_NAME}"
    REGISTRY_CREDS = "dockerhub"
  }
  agent any

  stages {
    stage('Cleanup workspace') {
      steps {
        script {
          cleanWs()
        }
      }
    }
  }
}

  stages {
    stage('Cleanup workspace') {
      steps {
        script {
          cleanWs()
        }
      }
    }
  }

  stage(checkout SCM)
  steps{
    script{
      git branch: 'main',
      url: 'https://github.com/Mark-1305/gitopops-argocd.git'
    }
  }
  stage('Build Docker image'){
    steps{
      script
      docker_image = docker.build "$(IMAGE_NAME)"
    }
  }

