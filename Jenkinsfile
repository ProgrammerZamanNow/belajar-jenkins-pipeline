pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Hello Build 1'
                echo 'Hello Build 2'
                echo 'Hello Build 3'
                script {
                    for (int i = 0; i < 10; i++) {
                        echo("Script ${i}")
                    }
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Hello Test'
            }
            bat(mvn test)
        }
        stage('Deploy') {
            steps {
                echo 'Hello Deploy'
                sleep(5)
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