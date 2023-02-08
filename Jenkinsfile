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
        sh '''./mvnw sonar:sonar \\
  -Dsonar.host.url=http://44.212.59.25:9000/ \\
  -Dsonar.projectKey=jpetstore-6 \\
  -Dsonar.login=sqp_e881d98144f7a9d6747841ffa4ffd72efa4f6656'''
      }
    }

  }
}