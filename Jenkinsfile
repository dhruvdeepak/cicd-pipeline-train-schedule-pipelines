pipeline {
  agent any
  stages {
    stage ('Build') {
      steps {
        echo 'Running build automation'
        node { distBaseUrl = 'https://direct.nodejs.org/dist/' }
        sh './gradlew build --no-daemon'
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
        
      }
    }
  }
}
