
pipeline {
  agent any
  tools {
    maven 'maven'
    jdk 'JDK1.8'
  }
  stages {
    stage('Build') {
      steps {
        sh "mvn -B -DskipTests clean install"
      }
    } 
    /*stage('Start Sonar') {
      steps {
        sh "mvn sonar:sonar \
            -Dsonar.projectKey=SampleMavenPipeline \
            -Dsonar.host.url=http://54.202.172.93:9090 \
            -Dsonar.login=0d06e8fe62d9f8a4293001b7bf38a754dfe06325"
      }
    }*/
  }
}
   
  
