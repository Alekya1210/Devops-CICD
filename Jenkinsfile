pipeline {
  agent {
    node {
      label 'slave'
    }

  }
  stages {
    stage('git-checkout') {
      steps {
        git(url: 'https://github.com/Ram8319/Devops-CICD.git', branch: 'main', credentialsId: 'git-token')
      }
    }

    stage('maven-compile') {
      steps {
        sh 'mvn clean compile'
      }
    }

  }
}