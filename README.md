# MavenDeploy
Jenkins
in Build section
Execute shell
mvn deploy -Dversion=$version

Post-build Actions

Build Triggers	
Projects to build	->Nexus2DockerDeploy

Trigger when build is	->Stable

########jenkins with parameter###########

This project is parameterized	Help for feature: This project is parameterized
String Parameter
[Help]
Name->	version
 Default Value->$version

  
Build
Execute shell
[Help]
 	Command	

echo $version
 
  ##############
  
