timestamps {
    node () {
		stage('Clean up Workspace') {
			deleteDir()
		}	    
        	
	    stage ('CloneGitHub Repository') {
        	checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/ashbtivish/nodejsawslambda.git']]]) 
        }

		stage ('SonarQube Scanner') {
			sh '''
				/opt/scanner/bin/sonar-scanner \
  -Dsonar.projectKey=nodejssample \
  -Dsonar.sources=.
			'''
		}
		
		stage ('Packaging Application') {
		    sh "serverless deploy"
		}
    }
}
