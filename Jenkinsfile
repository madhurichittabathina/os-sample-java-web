pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        bat 'mvn install'
        git(url: 'https://github.com/madhurichittabathina/os-sample-java-web.git', branch: 'master')
      }
    }
    stage('build') {
      steps {
        bat 'mvn install'
      }
    }
    stage('sonarqube') {
      steps {
        bat 'mvn sonar:sonar'
      }
    }
  }
}