node{
// demo
   stage('SCM Checkout'){
     git 'https://github.com/sundarrajboobalan/example-tomcat-war.git'
   }
    stage('Compile-Package'){
      // Get maven home path
      def mvnHome =  tool name: 'maven', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
    }
    stage('SonarQube Analysis') {
        def mvnHome =  tool name: 'maven', type: 'maven'
        withSonarQubeEnv('sonarqube') { 
          sh "${mvnHome}/bin/mvn sonar:sonar"
        }
    }
}



