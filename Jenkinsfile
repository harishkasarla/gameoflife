pipeline {
  agent any
  stages {
    stage('Checkout') {
      parallel {
        stage('Checkout') {
          steps {
            sh 'mvn validate'
          }
        }
        stage('Compile') {
          steps {
            sh 'mvn compile'
          }
        }
        stage('Test') {
          steps {
            sh 'mvn test'
          }
        }
      }
    }
    stage('Package') {
      steps {
        sh 'mvn clean package'
      }
    }
    stage('Install') {
      steps {
        sh 'mvn clean install'
      }
    }
  }
}