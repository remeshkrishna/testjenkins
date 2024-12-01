pipeline {
  agent any
  stages {
    stage('fetch git') {
      steps {
        git(url: 'https://github.com/remeshkrishna/testjenkins.git', branch: 'main')
      }
    }

    stage('install apache') {
      steps {
        sh 'sudo apt install -y apache2'
      }
    }

    stage('deploy app') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}