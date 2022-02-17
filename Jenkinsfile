pipeline {
  agent 'agent'
  tools {
    maven 'maven' 
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
            archiveArtifacts artifacts: 'target/**/*.*'
            
        }
    }
}
