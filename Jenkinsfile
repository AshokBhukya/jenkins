@Library('mylibrary') _

pipeline{

    agent any

     

    stages{
         
        stage('Git Checkout'){
             steps{
            gitCheckout(
                git branch: 'main', url: ' git@github.com:Shankargoud1/jenkins.git'
            )
            }
        }