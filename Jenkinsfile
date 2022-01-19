pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        retry(count: 3) {
          sh 'jhjh'
        }

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
        input(message: 'are you sure to deploy?', ok: 'Yes, I am sure')
        echo 'Deployment completed '
      }
    }

  }
}