
pipeline {
    agent any
    parameters{
        choice(name:'Version' , choices : ['1.1.0' , '1.2.0' ,'1.3.0'] , description : '')
    }

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
               sh """ cat REDAME.md """
               echo "check version ${params.version}"

            }
        
	}

		stage ('dep'){
	    when{
                branch "dep-*"
	    }
            steps {
               echo "check version ${params.version}"
				

            }
        
	}
		stage ('maim'){
	    when{
                branch "main*"
	    }
            steps {
               echo "check version ${params.version}"

            }
        
	}

    }

    post {
        success  {
            echo 'run good'
        }
    }
}




