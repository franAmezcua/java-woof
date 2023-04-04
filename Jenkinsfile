pipeline {
    agent any

    stages {
        stage("SNYK-OSS-Test"){
            steps{
		        echo 'Snyk OSS Scanning...'
		        snykSecurity(
		            snykInstallation: 'SnykV2PluginTest',
		            snykTokenId: 'SnykTkn',
		            severity: 'high',
		            additionalArguments: '--all-sub-projects -d',
		            failOnIssues: 'false'
		        )
		    }
        }
    }
}
