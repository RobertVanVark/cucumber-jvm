node {
   def mvnHome
   stage('Preparation') { // for display purposes
      mvnHome = tool 'mvn3'
   }
   stage('Pre-Build') {
      node {
         checkout scm
         echo "Pre-Build stage - $PATH"
      }
      node {
         echo "Pre-Build stage - $OSTYPE"
      }
   }
   stage('Build') {
//      sh "'${mvnHome}/bin/mvn' -Dmaven.test.failure.ignore clean package"
      echo 'Build stage' 
   }
   stage('Results') {
//      junit '**/target/surefire-reports/TEST-*.xml'
//      archive 'target/*.jar'
      echo 'Results stage'
   }
}
