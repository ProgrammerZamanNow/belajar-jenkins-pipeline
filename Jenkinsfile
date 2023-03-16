pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World From JenkinsFile Github'
            }
        }
    }

    post {
        always {
          echo "I will always say Hello again!"
        }
        success {
          echo "Yay, success"
        }
        failure {
          echo "Oh no, failure"
        }
        cleanup {
          echo "Don't care success or error"
        }
      }
}