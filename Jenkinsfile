pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ PES1UG21CS112-1.cpp -o PES1UG21CS112-1'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh './PES1UG21CS112-1'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
    }
    post {
          failure {
              echo 'Pipeline failed'
          }
      }
}
