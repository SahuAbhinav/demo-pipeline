pipeline{
  agent any
  stages{
  stage ('Build') {

    steps{
    git url: 'https://github.com/SahuAbhinav/m-job'

      // Run the maven build
      bat "mvn clean install"
    }
    post {
                success {
                    // we only worry about archiving the jar file if the build steps are successful
                    archiveArtifacts(artifacts: '**/target/*.jar', allowEmptyArchive: true)
                }
            }
  }
  }
}
