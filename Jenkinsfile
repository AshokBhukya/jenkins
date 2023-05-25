@Library('mylibrary') _

pipeline{

    agent any

     

    stages{
         
        stage('Git Checkout'){
             steps{
            gitCheckout(
                git branch: 'main', credentialsId: 'jenkins', url: ' git@github.com:Shankargoud1/jenkins.git'
            )
            }
        }