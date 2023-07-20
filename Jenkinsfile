pipeline {
  agent { label 'aws cloud node1' }
  parameters {
               choice choices: ['Dev', 'Test', 'UAT'], description: 'this  is environment parameter', name: 'environment'
               string defaultValue: '8080', description: 'This is port for application', name: 'Port'
             }
  stages {
    stage('Checkout Repo') {
      steps {
        git branch: '${BRANCH_NAME}', url: 'https://github.com/cloud-dev-user/warehouse-application.git'
      }
    }
    stage('build CI stage ') {
      steps {
        sh 'mvn clean install '
      }
      }
       stage('Show the parameters ') {
      steps {
       echo '$environment'
      }
      }
    
}
}
