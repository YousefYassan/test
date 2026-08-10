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
                sh 'uname -a' 
            }
        }
        stage('sleep') {
            steps {
                sh 'sleep 5' 
            }
        }
    }

    post {
        always {
            echo 'run good'
        }
    }
}

