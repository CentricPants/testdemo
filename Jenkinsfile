pipeline {
  agent any

  stages {
    stage('Checkout') {
    steps {
        git branch: 'main',
            url: 'https://github.com/CentricPants/testdemo.git',
            credentialsId: 'github-token'
    }
}


    stage('Build') {
        steps {
            echo 'Building..'
        }
    }

    stage('Test') {
      steps {
        echo 'Testing..'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }
  }

  post {
    always {
      echo 'post build condition running'
    }
    failure {
      echo 'post action if build fail'
    }
  }
}
