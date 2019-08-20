pipeline {

  agent any
  
  stages {
    stage('Download Project') {
        
    }
    stage('Build Project') {
      build job: 'ComplexUI', propagate: false
    }
    stage('Test') {
      steps {
         sh label: '', script: 'cd ./../../../ComplexUI/NUnitTask2'
         sh label: '', script: 'dotnet test -l:trx'      
      }
    }
  }
}
