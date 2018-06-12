pipeline {
  agent none
  stages {
    stage('build') {
      parallel {
        stage('1') {
          agent { dockerfile { dir 'dir1' } }
          steps {
            sh 'cat /app/file'
          }
        }
        stage('2') {
          agent { dockerfile { dir 'dir2' } }
          steps {
            sh 'cat /app/file'
          }
        }
      }
    }
  }
}
