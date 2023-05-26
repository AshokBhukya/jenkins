@Library('myLibrary') _

pipeline{

    agent any

     tools {
    maven 'maven'
        }
     parameters{

        choice(name: 'action', choices: 'create\ndelete', description: 'Choose create/Destroy')
     }
    stages{
         
        stage('Git Checkout'){
            when { expression {  params.action == 'create' } }
             steps{
            gitCheckout(
                branch: "master",
                url: "git@github.com:Shankargoud1/java-hello-world-with-maven.git"
            ) 
            }
        }
        
      
      stage('Unit Test maven'){

        when { expression {  params.action == 'create' } }
         
            steps{
               script{
                   
                   mvnTest()
               }
            }
        }
      
        stage('Integration Test maven'){
          
          when { expression {  params.action == 'create' } }
             steps{
               script{
                   
                   mvnIntegrationTest()
               }
            }
        }
       

      stage('Static code analysis: Sonarqube'){
         when { expression {  params.action == 'create' } }
            steps{
               script{
                   
                   def  SonarQubecredentialsId = 'sonarqube-api'
                   statiCodeAnalysis(SonarQubecredentialsId)
               }
            }
        }

      stage(' maven Build'){
         
         when { expression {  params.action == 'create' } }
       
           steps{
               script{
                   
                   mvnBuild()
               }
            }
        }

    }
    }
