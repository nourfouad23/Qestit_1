node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'Scanner1';
    withSonarQubeEnv() {
       if (isUnix()) 
        sh "${scannerHome}/bin/sonar-scanner"
     else 
       bat "${scannerHome}/bin/sonar-scanner"      
    }
  }
}
