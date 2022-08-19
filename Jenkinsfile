pipeline {
  agent any
    
  tools {nodejs "node"}
    
  stages {
        
    stage('Git Pull') {
      steps {
        git url: 'https://github.com/AlexyPulivelil/testapp' branch: 'pipeline'
      }
    }
     
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }  
    
            
    stage('Test') {
      steps {
        sh 'ls -al'
      }
    }
  }
}