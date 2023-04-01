pipeline {
  agent any
  stages {
    stage('Maven Version') {
      parallel {
        stage('Maven Version') {
          steps {
            bat 'mvn -v'
          }
        }

        stage('Java Version') {
          steps {
            bat 'java -version'
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
