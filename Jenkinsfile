pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'ant -f hello-world-ant/build.xml -v'
      }	
    }
  }

  post {
    always {
      archiveArtifacts artifacts: 'dist/*.jar', fingerprint: true   
    }  
  }
}

