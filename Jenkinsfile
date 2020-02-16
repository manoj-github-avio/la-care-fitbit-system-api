pipeline {
  agent any
  stages {
    stage('MUnit Test') { 
      steps {
        sh 'mvn clean test'
      }
    }
    stage('Mule project Build') { 
      steps {
        sh 'mvn clean install'
      }
    }
    stage('Deploy CloudHub') { 
      steps {
        sh 'clean deploy -DmuleDeploy'
      }
    }
  }
}