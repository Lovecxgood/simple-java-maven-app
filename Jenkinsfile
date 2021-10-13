pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'build'
      }
    }

    stage('Test') {
      parallel {
        stage('windows') {
          steps {
            echo 'windows'
          }
        }

        stage('linux') {
          steps {
            echo 'linux'
          }
        }

        stage('macos') {
          steps {
            echo 'macos'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'deploy'
      }
    }

  }
  environment {
    image = 'maven:3-alpine'
    args = '-v /root/.m2:/root/.m2'
  }
}