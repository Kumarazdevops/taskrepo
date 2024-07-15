pipeline {
  agent any

  stages{
    stage('git clone'){
      steps{
        git branch : 'master', url: 'https://github.com/Kumarazdevops/taskrepo.git'
      }
    }
    stage('Build image'){
      steps{
        bat 'docker build -t myimage .'
      }
    }
  }
}
