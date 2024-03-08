pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                checkout scm
                script {
                    // Print contents of workspace directory
                    sh 'ls -la'
                }
            }
        }
        
        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file using a shell script
                    sh 'g++ -o output_executable source_code.cpp'
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    // Print the output of the compiled executable
                    sh './output_executable'
                }
            }
        }
    }
    
    post {
        always {
            // Display 'pipeline failed' in case of any errors within the pipeline
            catchError {
                echo 'Pipeline succeeded'
            }
        }
    }
}
