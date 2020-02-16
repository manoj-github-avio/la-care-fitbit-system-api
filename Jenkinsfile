pipeline {
  agent any
  tools {
  maven "Maven-3.6.3"
  }
  stages {
    stage('Mule project Build') { 
      steps {
        sh 'mvn clean install'
      }
    }
    stage('MUnit Test') { 
      steps {
        sh 'mvn test'
      }
    }
    stage('Deploy CloudHub') { 
      steps {
        sh 'mvn clean deploy -DmuleDeploy'
      }
    }
  }
}