pipeline {
  agent any
    
  tools {nodejs "Nodejs"}
    
  stages {
        
    stage('Git Pull') {
      steps {
        git url: 'https://github.com/AlexyPulivelil/testapp', branch: 'pipeline'
      }
    }
     
    stage('Build') {
      steps {
        sh 'npm build'
      }
    }  
    
            
    stage('Test node versions') {
      steps {
        sh 'node -v'
      }
    }
  }
}