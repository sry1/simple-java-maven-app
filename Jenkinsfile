pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
        sh 'jenkins/build.sh'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing'
        junit 'target/**/*.xml'
        sh 'jenkins/test-all.sh'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying'
        sh 'jenkins/deploy.sh'
      }
    }

  }
}