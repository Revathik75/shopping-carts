pipeline {
  agent any
  stages {
    stage('build-the-app') {
      steps {
        echo 'this is the first job'
        sh 'mvn compile'
      }
    }

    stage('test-the-app') {
      steps {
        echo 'this is the second job'
        sh 'mvn clean test'
      }
    }

    stage('package-the-app') {
      steps {
        echo 'this is the third job'
        sh 'mvn package -DskipTests'
      }
    }

    stage('archive') {
      steps {
        archiveArtifacts '**/target/*.jar'
      }
    }

  }
  tools {
    maven 'maven'
  }
  post {
    always {
      echo 'my pipeline has completed...'
    }

  }
}