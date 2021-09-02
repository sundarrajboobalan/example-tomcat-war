node{
  stage('SCM Checkout') {
    git 'https://github.com/sundarrajboobalan/example-tomcat-war'
  }
  stage('Build') {
    def mvnHome= tool name: 'maven3', type: 'maven'
    sh "${mvnHome} /bin/mvn package"
      }
}
