node {
   def mvnHome
   stage('Preparation') { // for display purposes
      mvnHome = tool 'mvn3'
   }
   stage('Build') {
      checkout scm
      sh "'${mvnHome}/bin/mvn' -Dmaven.test.failure.ignore clean package"
   }
   stage('Results') {
      junit '**/target/surefire-reports/TEST-*.xml'
      archive 'target/*.jar'
   }
}
