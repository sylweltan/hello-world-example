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
        sh 'echo "Jestę resultatem"'
        echo 'DingoDongoBam'
      }
    }

    stage('') {
      steps {
        archiveArtifacts 'target/*.jar'
      }
    }

  }
  post {
    always {
      sh 'echo "Post action. Dziękuję i dobranoc."'
    }

  }
}