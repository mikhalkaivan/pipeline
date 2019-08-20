pipeline {

  agent any
  
  stages {
    stage('Download Project') {
        git branch: 'Task2_NUnit', credentialsId: '271d0ce9-68eb-46a9-beb3-c1f4fc88dbc8', url: 'http://git01.godeltech.com/A-QA_Mastery/i_mikhalka/mytasks.git'
    }
    stage('Build Project') {
      echo 'from build stage'
    }
    stage('Test') {
      steps {
         sh label: '', script: 'cd NUnitTask2'
         sh label: '', script: 'dotnet test -l:trx'      
      }
    }
    stage('Post Build'){
      steps {
        mstest()
      }
    }
  }
}
