pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build completed'
      }
    }

    stage('Test stages') {
      parallel {
        stage('Test 2') {
          steps {
            echo 'Test2 running '
          }
        }

        stage('test1') {
          steps {
            echo 'test1 running'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deployment completed '
      }
    }

  }
}