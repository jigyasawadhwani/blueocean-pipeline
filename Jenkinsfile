pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'echo "build"'
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'testing'
          }
        }

        stage('cq') {
          steps {
            echo 'quality check'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        sh 'echo "deploy"'
      }
    }

  }
}