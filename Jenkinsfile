pipeline {
agent any 
  tools {
  maven 'maven'
  }
  stages{
    stage('git-clone'){
      steps {
    checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'GitHUB-CREDENTIALS', url: 'https://github.com/ralphizuike/etech_web_app']]])
    }
    }
    stage('check-user'){
      steps{
        sh ' cat /etc/passwd '
      }
    }
    stage('k8s-test'){
      steps{
     withKubeConfig(caCertificate: '', clusterName: '', contextName: '', credentialsId: 'kubesecrete', namespace: '', serverUrl: '') {
       sh ' kubectl get ns '
    // some block
}
      }
    }
  }
}
