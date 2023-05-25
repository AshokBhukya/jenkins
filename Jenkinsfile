@Library('mylibrary') _

pipeline{

    agent any

     tools {
    maven 'mvn'
  }

    stages{
         
        stage('Git Checkout'){
             steps{
            gitCheckout(
                branch: "main",
                url: "git@github.com:Shankargoud1/jenkins.git"
            )
            }
        }
        stage('Unit Test maven'){
         
          

            steps{
               script{
                   
                   mvnTest()
               }
            }
        }
    }
    }
