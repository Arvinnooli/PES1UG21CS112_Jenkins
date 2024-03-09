pipeline {
    agent any

    stages {
        stage('Clone repository') {
            steps {
                git branch: 'main',
                url: 'https://github.com/Arvinnooli/PES1UG21CS112_Jenkins.git'
                echo 'in Clone'
            }
        }

        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file using a shell script
                    sh 'g++ -o my_executable ${WORKSPACE}/main/hello.cpp'
                    echo 'in Build'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Print output of the compiled .cpp file
                    sh './my_execute'
                    echo 'in Test'
                }
            }
        }

        stage('Deploy'){
            steps {
                script {
                    echo 'Deploy successful Arvin'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed Arvin'
        }
    }
}
