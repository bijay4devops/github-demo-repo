pipeline {
  agent any

  tools{
    maven 'localMaven'
    jdk 'localJDK'
  }
  environment {
    fname = "Bijay"
    lname = "Mahakuda"
    version = "1.2"
    system = "test"
  }
  stages{
    stage('Build'){
      steps{
        sh 'mvn clean package'
      }
      post {
            success {
              echo 'archiving the artifacts'
              archiveArtifacts artifacts: '**/target/*.jar'
            }
      }
    }
    stage ('Deploy to string'){
      steps {
        echo 'This is just a demo on string server.'
      }
    }
  }
}
