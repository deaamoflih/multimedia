node {
  
  
  stage('SCM') {
    checkout([$class: 'GitSCM', branches: [[name: '*/new']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/deaamoflih/multimedia']]])
                }
  stage('Build and Anlyzing multi') {
  
        withSonarQubeEnv('sonarqube') {
         def scannerHome = tool 'sonarqube';
  
       sh "${scannerHome}/bin/sonar-scanner -Dsonar.projectName='desfsgv' -Dsonar.projectKey='ddsfsfev' -Dsonar.sources='./' -Dsonar.language=java -Dsonar.java.binaries=* -Dsonar.branch.name=neddw -Dsonar.scm.disabled=true " 
  
           
                }
  }

    
  }
