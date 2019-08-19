pipeline {

  node { build job: 'ComplexUI', propagate: false

    sh label: '', script: 'cd ./../../../ComplexUI/NUnitTask2'

    sh label: '', script: 'dotnet test -l:trx'
  }

}
