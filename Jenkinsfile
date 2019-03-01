
pipeline {
  agent any
  tools {
    maven 'Maven'
    jdk 'java1.8.0'
  }
  stages {
    stage('Build') {
      steps {
        sh "mvn -B -DskipTests clean package"
      }
    }
    stage('Unit Test') {
      steps {
        sh 'mvn test'
      }
    }
    stage('Deploy') {
      steps {
        sh 'java -jar target/my-app-1.0-SNAPSHOT.jar'
      }
    }    
  }
}
   
  
