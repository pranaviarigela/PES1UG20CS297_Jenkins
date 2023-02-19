pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ temp.cpp -o temp'
                 build job: 'PES1UG20CS297-1', wait: false
                 echo 'Build by CS297 successful'
            }
        }

        stage('Test') {
            steps {
                sh 'cat temp.cpp'
                echo 'Test by CS297 successful'
            }
        }

        stage('Deploy') {
            steps {
               
                echo 'Deploy by CS297 successful'
            }
        }
    }

    post {
        failure {
            
                ehco 'Pipeline Failed'
          
        }
    }
}
