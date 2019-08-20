pipeline {
  
  agent any
  
  stages {
    stage('Download Project') {
      steps {
        echo 'from download project stage'
        git branch: 'Task2_NUnit', credentialsId: '271d0ce9-68eb-46a9-beb3-c1f4fc88dbc8', url: 'http://git01.godeltech.com/A-QA_Mastery/i_mikhalka/mytasks.git'
      }        
    }
    stage('Build Project') {
      steps {
         echo 'from build stage'
         sh label: '', script: 'dotnet build NUnitTask2/NUnitTask2.sln'     
      }
    }
    stage('Test') {
      steps {
         echo 'from test stage'
         sh label: '', script: 'pwd'
         sh label: '', script: 'cd NUnitTask2'
         sh label: '', script: 'ls -a'
         sh label: '', script: 'dotnet test NUnitTask2/NUnitTask2.sln --no-build -l:trx'      
      }
    }
    stage('Post Build'){
      steps {
        echo 'from post build stage'
        mstest()
      }
    }
  }
}
