
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
                echo 'OS'
                sh 'uname -a'
                echo 'Memory'
                sh 'systeminfo | grep "Total Physical Memory"'
                echo 'space'
                sh 'df -h'
            }
        }

	stage('redme') {
	when{
      branch "main"
	}

            steps {
                sh """ cat REDAME.md    """"
            }
        }


       stage('end') {
            steps {
                echo 'end of file'
            }
        }
    }
}

