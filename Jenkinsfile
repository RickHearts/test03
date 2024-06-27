pipeline {
  agent any
  stages {
    stage('Chrome') {
      parallel {
        stage('Chrome') {
          steps {
            echo 'Chrome TEST'
          }
        }

        stage('Firefox') {
          steps {
            echo 'FirefoxTest'
          }
        }

      }
    }

    stage('Build & Test') {
      steps {
        sh 'echo "My file" > a.out'
        bat 'mvn package'
      }
    }

    stage('Deploy') {
      steps {
        pwd(tmp: true)
        git(url: 'https://github.com/RickHearts/mvn1', branch: 'main')
      }
    }

  }
}