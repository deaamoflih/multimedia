node {
  
  
  stage('SCM') {
    checkout([$class: 'GitSCM', branches: [[name: '*/new']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/deaamoflih/multimedia']]])
                }
  stage('Build and Anlyzing multi') {
  
        withSonarQubeEnv('sonarqube') {
        def mvnHome = tool name: 'mvn', type: 'maven' 
         def scannerHome = tool 'sonarqube';
  
       sh "${scannerHome}/bin/sonar-scanner -Dsonar.projectName='dev' -Dsonar.projectKey='dev' -Dsonar.sources='./' -Dsonar.language=java   " 
  
           
                }
  }

    
  }
