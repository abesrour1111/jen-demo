pipeline {
  agent any
  stages {
    stage('stage1') {
      parallel {
        stage('stage1') {
          steps {
            sh 'scho "ok" > /tmp/git'
          }
        }

        stage('stage1p') {
          steps {
            sh 'echo "ok2" >/tmp/git2'
          }
        }

      }
    }

    stage('stag2') {
      steps {
        sh '''grep ok /tmp/git
grep ok /tmp/git2'''
      }
    }

  }
}