pipeline {
    agent any

     parameters{
      choice (name:'VERSION' , choices:['1.1.0','1.2.0','1.3.0'],description : '')

     }


    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('check') {
            steps{
                    echo 'check out sys dev'
		    echo "check version ${VERSION}"
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

