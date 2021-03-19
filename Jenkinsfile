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
./create_deployment_package.sh 
 """ 
	}
}
}