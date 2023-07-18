pipeline {
  agent { label 'aws cloud node1' }
  stages {
    stage('Checkout Repo') {
      steps {
        git branch: 'feature/cicd', url: 'https://github.com/cloud-dev-user/warehouse-application.git'
      }
    }
    stage('build CI stage ') {
      steps {
        sh 'mvn clean install '
      }
    }

  }
}
