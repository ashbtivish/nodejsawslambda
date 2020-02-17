node {
  def runSonarScan(nodejssample){
      withEnv(['SONAR_HOST=' + '']) {
          sh '''
          $/opt/sonarqube/sonar-runner-2.4/bin/sonar-runner -e -Dsonar.projectkey=nodejssample
          '''
      }
  }
}
