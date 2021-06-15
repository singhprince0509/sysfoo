pipeline {
  agent any
  
  tools{
      maven 'Maven 3.6.3'
  }
  
  stages{
      stage("build"){
          steps{
              echo 'compile sysfoo app'
              sh 'mvn compile'
              sleep 3
          }
      }
      stage("test"){
          steps{
              echo 'running unit tests'
              sh 'mvn clean test'
              sleep 9
          }
      }
      stage("package"){
          steps{
              echo 'package app to generate artifacts'
              sh 'mvn package -DskipTests'
              sleep 5
          }
      }
  }

  post{
    always{
        echo 'This pipeline is completed..'
    }
  }
}
