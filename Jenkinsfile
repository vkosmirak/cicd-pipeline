pipeline {
  agent {
    dockerfile {
      filename 'Dockerfile'
    }

  }
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            script {
              scripts/build.sh
            }

          }
        }

        stage('Test step') {
          steps {
            script {
              ls
            }

          }
        }

      }
    }

    stage('Test') {
      steps {
        sh 'scripts/test.sh'
      }
    }

  }
}