node {
  stage('SCM Checkout') {
    git 'https://github.com/sundarrajboobalan/example-tomcat-war'
  }
  stage('Compile-Package') {
    sh 'mvn package'
  }
}
