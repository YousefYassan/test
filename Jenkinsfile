

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
 stage('dep-1') {
            steps {
               echo 'sleep 2'
            }
                }
                        stage ('dep'){
            when{
                branch "dep-1*"
            }
            steps {
               sh """ cat REDAME.md """
            }

        }

     }

    post {

        always {
            echo 'run good gg'
        }
    }

}
