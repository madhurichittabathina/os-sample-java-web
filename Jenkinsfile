pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        bat(script: 'https://github.com/madhurichittabathina/os-sample-java-web.git', label: 'master')
      }
    }
  }
}