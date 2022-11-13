pipeline {
  agent any
  stages {
    stage('fetch') {
      steps {
        git(url: 'https://github.com/Vinayak341/pipeline.git', branch: 'main', poll: true)
      }
    }

    stage('install apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('deploy') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}