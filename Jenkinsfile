pipeline {
  agent any
  stages {
    stage('code') {
      steps {
        echo 'This is the Code stage'
      }
    }

    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh '''date
cal

'''
          }
        }

        stage('Build1') {
          steps {
            echo 'This is a parallel stage'
          }
        }

        stage('Build2') {
          steps {
            build 'test1'
          }
        }

      }
    }

    stage('Final') {
      steps {
        echo 'This is the final step'
      }
    }

  }
}