// Powered by Infostretch 

timestamps {

node () {

	stage ('awsbuild - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'awsbuild', url: 'https://github.com/oleksiisavin/awsbuild.git']]]) 
	}
	stage ('awsbuild - Build') {
 			// Shell build step
sh """ 
mvn -version 
ls -la
#./create_deployment_package.sh
#/opt/aws-codebuild-docker-images/local_builds/codebuild_build.sh -a artifact -i aws/codebuild/standard:3.0 -c -b buildspec.yml 
 """ 
	}
}
}
