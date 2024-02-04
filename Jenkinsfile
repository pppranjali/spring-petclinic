pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        sh './mvnw clean compile'
      }
    }

    stage('Static Analysis') {
      steps {
        sh '''./mvn clean verify sonar:sonar \\
  -Dsonar.projectKey=Petclinic \\
  -Dsonar.projectName=\'Petclinic\' \\
  -Dsonar.host.url=http://52.66.221.113:9000 \\
  -Dsonar.token=sqp_5090c33d7e6c88be34587aad1bc7640f30843e13'''
      }
    }

  }
}