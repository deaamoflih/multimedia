node {
  
  
  stage('SCM') {
    checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/deaamoflih/multimedia']]])
                }
  stage('Build and Anlyzing multi') {
      withMaven {
        withSonarQubeEnv('sonarqube') {
        def mvnHome = tool name: 'mvn', type: 'maven' 
         def scannerHome = tool 'sonarqube';
  
        sh "${mvnHome}/bin/mvn clean verify sonar:sonar "
  
                }
                }
  }

    
  }
