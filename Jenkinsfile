pipeline{
    agent any
	stages{
	
		stage('Build Application'){
			steps{
			bat 'mvn clean install'		
			}
		}
		
		stage('Deploy Application - CloudHub'){		
			steps{
				bat 'mvn package deploy -DmuleDeploy -DskipTests -Dmule.version=4.3.0 -Danypoint.username=manju_kaushik_april2021 -Danypoint.password=kMa6Dfe007 -Danpoint.environment=Sandbox -Danpoint.workerType=Micro -Danpoint.workers=1 -Danpoint.applicationName=WorldTimeDeployChub'
				}
		}

	}
}