pipeline {
  agent any
    
  tools {nodejs "node"}
    
  stages {
        
    stage('Git') {
      steps {
        git changelog: false, credentialsId: 'github', poll: false, url: 'https://github.com/AlexyPulivelil/testapp'
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