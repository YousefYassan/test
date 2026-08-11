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
                // 🟢 سيعمل الآن مباشرة كأمر bash طبيعي بعد إعادة التشغيل
                  echo 'check out sys dev' 
            }
       }
        stage('sleep') {
            steps {
                sh 'sleep 2' 
            }
        }
    }

    post {
        always {
            echo 'run good'
        }
    }
}

