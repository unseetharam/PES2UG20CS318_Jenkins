pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ temp.cpp -o temp'
                 build job: 'PES2UG20CS318-1', wait: false
                 echo 'Build by CS318 successful'
            }
        }

        stage('Test') {
            steps {
                sh 'cat temp.cpp'
                ech 'Test by CS318 successful'
            }
        }

        stage('Deploy') {
            steps {
               
                echo 'Deploy by CS318 successful'
            }
        }
    }

    post {
        failure {
            
                echo 'Pipeline Failed'
          
        }
    }
}
