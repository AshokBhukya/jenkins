@Library('myLibrary') _

pipeline{

    agent any

     tools {
    maven 'maven'
  }

    stages{
         
        stage('Git Checkout'){
             steps{
            gitCheckout(
                branch: "master",
                url: "git@github.com:Shankargoud1/java-hello-world-with-maven.git"
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
      
        stage('Integration Test maven'){
 
             steps{
               script{
                   
                   mvnIntegrationTest()
               }
            }
        }

      stage(' maven Build'){
       
           steps{
               script{
                   
                   mvnBuild()
               }
            }
        }

    }
    }
