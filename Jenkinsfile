pipeline {
    agent any
    tools {
        maven "MAVEN"
        jdk "JDK"
    }
    stages {
        stage('Initialize'){
            steps{
                echo "PATH = ${M2_HOME}/bin:${PATH}"
                echo "M2_HOME = /opt/maven"
            }
        }
        stage('Build') {
            steps {
                
                sh 'mvn -B -DskipTests clean package'
                
            }
        }
        stage('Deploy') {
            steps {
                sshagent(['deploy']) {
   sh 'scp -o StrictHostKeyChecking=no /demoo_master/target/Testt-0.0.1-SNAPSHOT.jar ubuntu@13.55.100.146:/opt/tomcat/webapps'
}
                
            }
        }
     }
  
}
