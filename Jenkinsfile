pipeline {
  agent any
  stages {
    stage('Maven Version') {
      parallel {
        stage('Maven Version') {
          steps {
            sh 'mvn -v'
          }
        }

        stage('Java Version') {
          steps {
            sh 'java -version'
          }
        }

      }
    }

    stage('Build') {
            steps {
                
                sh 'mvn -B -DskipTests clean package'
                
            }
        }

  }
}
