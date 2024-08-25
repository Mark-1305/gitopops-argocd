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
NU"

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
