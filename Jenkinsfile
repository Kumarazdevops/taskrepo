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
    stage('Container'){
        steps{
            bat "docker run -d --name testcont -p 8084:80 myimage"
        }
    }
  }
}
