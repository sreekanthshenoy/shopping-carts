pipeline {
  agent any
  stages {
    stage('build-the-app') {
      steps {
        echo 'this is the build job'
        sh 'mvn compile'
      }
    }

    stage('test-the-app') {
      steps {
        echo 'this is the test job'
        sh 'mvn clean test'
      }
    }

    stage('package-the-app') {
      steps {
        echo 'this is the package job'
        sh 'mvn package -DskipTests'
      }
    }

    stage('create-deployable') {
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
      echo 'this pipeline has completed...'
    }

  }
}