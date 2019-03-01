
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
    stage('Unit Test123') {
      steps {
        sh 'mvn test'
      }
      post {
        always {
          junit 'target/surefire-reports/*.xml'
        }
      }
    }
    stage('Upload to JFrog') {
      steps {
        sh 'curl -X PUT -u admin:AP8UM6UyW1i4xpPQceU7t8dyT6Y -T target/my-app-1.0-SNAPSHOT.jar "http://34.215.7.154:8081/artifactory/example-repo-local/my-app-1.0-SNAPSHOT.jar"'
      }
    }
    stage('Deploy') {
      steps {
        sh 'java -jar target/my-app-1.0-SNAPSHOT.jar'
      }
    }    
  }
}
   
  
