pipeline {
   agent { label 'master'}
   stages{
       stage('Init') { // for display purposes
          // Get some code from a GitHub repository
          steps{
          bat 'echo step1'
          }
          // Get the Maven tool.
          // ** NOTE: This 'M3' Maven tool must be configured
          // **       in the global configuration.           
       }
       stage('Build') {
          // Run the maven build
          steps{
          bat 'echo step2'
          }
       }
       stage('Deploy') {
           steps{
          bat 'echo step3'
           }
       }
   }
}