pipeline {
  agent any
  stages {
    stage('Init') {
      steps {
        sh './mvnw clean package'
      }
    }

    stage('Sonar') {
      steps {
        sh '''mvn clean verify sonar:sonar \\
  -Dsonar.projectKey=projet1 \\
  -Dsonar.host.url=http://localhost \\
  -Dsonar.login=333ab621c89a47f40a909b1a086ed31f6a2b1b23'''
      }
    }

  }
}