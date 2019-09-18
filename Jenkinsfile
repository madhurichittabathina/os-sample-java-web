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
    stage('deploy') {
      steps {
        bat 'xcopy "C:\\Program Files (x86)\\Jenkins\\workspace\\os-sample-java-web_master\\target\\ROOT.war" "C:\\Program Files\\Apache Software Foundation\\Tomcat 8.5\\webapps"'
      }
    }
  }
}