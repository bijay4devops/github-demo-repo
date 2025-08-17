pipeline {
  agent any

  tools{
    maven 'localMaven'
    jdk 'localJDK'
  }
  enviroment {
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
              archiveArtifacts artifacts: '**/target/*.war'
            }
      }
    }
    stage ('Deploy to string1'){
      steps {
        echo 'This is just a demo on string server.'
      }
    }
  }
}
