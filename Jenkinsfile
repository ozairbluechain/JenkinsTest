pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building...'
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Testing...'
          }
        }

        stage('Integration tests') {
          steps {
            echo 'Running integration tests...'
          }
        }

        stage('Performance tests') {
          steps {
            timeout(time: 90) {
              echo 'Running integration tests...'
            }

          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying...'
      }
    }

  }
}