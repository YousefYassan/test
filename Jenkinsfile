

pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('check') {
            steps {
                  echo 'check out sys dev'
            }
       }
        stage('sleep') {
            steps {
               echo 'sleep 2'
            }
                }
                        stage ('dev'){
            when{
                branch "dev-*"
            }
            steps {
               sh """ cat README.md """
            }

        }

     }

    post {

        always {
            echo 'run good'
        }
    }

}
