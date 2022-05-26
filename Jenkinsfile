pipeline {
agent any 
  tools {
  maven 'maven'
  }
  stages{
    stage('git-clone'){
      steps {
    checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-id', url: 'https://github.com/ralphizuike/etech_web_app']]])
    }
    }
  }
}
