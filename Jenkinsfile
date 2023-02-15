pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ temp.cpp -o temp'
                 build job: 'PES1UG20CS181-1', wait: false
                 echo 'Build by CS273 successful'
            }
        }

        stage('Test') {
            steps {
                sh 'cat temp.cpp'
                echo 'Test by PES1UG20CS181 successful'
            }
        }

        stage('Deploy') {
            steps {
               
                echo 'Deploy by PES1UG20CS181 successful'
            }
        }
    }

    post {
        failure {
            
                echo 'Pipeline by PES1UG20CS181 Failed'
          
        }
    }
}
