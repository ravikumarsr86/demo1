pipeline {
  agent any
  tools {
    maven '3.8.4' 
  }
  stages {
    stage ('Build') {
      steps {
        sh 'mvn clean package'
      }
    }
  }
    
     post {
        always {
            archiveArtifacts artifacts: 'target',
            junit 'target/**'
        }
    }
}
