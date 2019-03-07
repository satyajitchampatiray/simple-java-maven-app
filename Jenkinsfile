
pipeline {
  agent any
  tools {
    maven 'SampleMaven'
    jdk 'JDK1.8'
  }
  stages {
    stage('Build') {
      steps {
        sh "mvn -B -DskipTests clean install"
      }
    }     
  }
}
   
  
