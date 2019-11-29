pipeline {
  agent {
    node {
      label 'test'
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
}