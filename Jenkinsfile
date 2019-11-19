pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'mvn clean package'
            }
        }
        stage {
          steps {
            archiveArtifacts artifacts: 'target/*.war', fingerprint: true
            
        }   
    }
  }
}
