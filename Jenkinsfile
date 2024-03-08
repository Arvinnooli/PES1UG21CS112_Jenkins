pipeline {
  agent {
    docker{
      image 'node:14'
    }
  }
stages{
  stage('Clone repository') {
    steps {
      git branch: 'main',
        URL: 'https://github.com/Arvinnooli/PES1UG21CS112_Jenkins.git'
    }
  }
  stage('Install depemdencies'){
    steps{
      sh 'npm install'
    }
  }
  
