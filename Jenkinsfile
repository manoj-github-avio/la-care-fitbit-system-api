pipeline {
  agent any
  stages {
    stage('MUnit Test') { 
      steps {
        sh 'clean test'
      }
    }
    stage('Mule project Build') { 
      steps {
        sh 'clean install'
      }
    }
    stage('Deploy CloudHub') { 
      steps {
        sh 'clean deploy -DmuleDeploy'
      }
    }
  }
}