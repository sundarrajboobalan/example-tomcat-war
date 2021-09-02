node{
stage('SCM Checkout') {
git 'https://github.com/sundarrajboobalan/example-tomcat-war'
}
stage('Compile-Package') {
def mvnHome = tool name: 'maven3', type: 'maven'
sh "${mvnHome}/bin/mvn package"
}
}
