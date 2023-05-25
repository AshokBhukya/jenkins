@Library('mylibrary') _

pipeline{

    agent any

     tools {
    maven 'maven'
  }

    stages{
         
        stage('Git Checkout'){
             steps{
            gitCheckout(
                branch: "main",
                url: "git@github.com:Shankargoud1/spring-boot-war-example.git"
            )
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
