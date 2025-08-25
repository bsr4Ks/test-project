node {
    stage('SCM') {
    checkout scm
  }

    stage('Example') {
        sh "echo 'jenkins starts!'"
    }

    stage('SonarQube Analysis') {
    def scannerHome = tool 'SonarScanner';
    withSonarQubeEnv() {
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}