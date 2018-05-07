
pipeline {
   agent { label 'master'}
   tools {
    maven 'localMaven'
    }
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
          bat 'mvn clean package'
          }
          post{
            success{
                bat 'echo Now Archiving..,'
                archiveArtifacts artifacts: '**/target/*.war'
            }
          }
       }
       stage('Deploy to staging') {
           steps{
          bat 'echo step3'
          build job: 'Deploy-to-staging'
           }
       }

   }
}