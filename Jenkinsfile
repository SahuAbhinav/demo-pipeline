pipeline{
  agent any
  stages{
  stage ('Build') {

    steps{
    git url: 'https://github.com/SahuAbhinav/m-job'

      // Run the maven build
      bat 'mvn clean install'
    }
    post {
                success {
                   echo 'build success'
                   
                }
            }
  }
  }
}
