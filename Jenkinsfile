pipeline {
    agent any
    stages {
        stage('package') {
            steps {
                sh 'mvn clean package'
            }
        }
    }

    post {
        always {
          archiveArtifacts artifacts: 'target/*.war', fingerprint: true  
        }
    }
}
