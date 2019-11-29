pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('Build') {
      steps {
        withMaven(maven: 'M3', publisherStrategy: 'EXPLICIT') {
          sh 'mvn clean install'
        }

      }
    }

    stage('Results') {
      steps {
        sh 'echo "ala"'
      }
    }

  }
  finally {
    always {
      sh 'echo "ala"'
    }
  }
}
