@Library('mylibrary') _

pipeline{

    agent any

     

    stages{
         
        stage('Git Checkout'){
             steps{
            gitCheckout(
                branch: "main",
                url: "git@github.com:Shankargoud1/jenkins.git"
            )
            }
        }