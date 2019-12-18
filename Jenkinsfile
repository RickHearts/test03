pipeline {
  agent any
  stages {
    stage('Chrome') {
      parallel {
        stage('Chrome') {
          steps {
            echo 'Chrome Tests'
            sleep 15
          }
        }

        stage('Firefox') {
          steps {
            echo 'Firefox Test'
          }
        }

      }
    }

    stage('Edge') {
      steps {
        sleep 15
        echo 'Edge Test'
        input(message: 'Do you want to continue', ok: 'continue')
      }
    }

  }
}