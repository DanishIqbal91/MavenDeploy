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
 
 ###############
change pom.xml 
<distributionManagement>
<repository>
<id>devrepo</id>
<name>Internal Repository</name>
<url>http://192.168.162.31:8081/#browse/browse/components:maven-snapshots</url>
</repository>

 <snapshotRepository>
     <id>Snapshots</id>
     <name>snapshotRepo</name>
     <url>http://192.168.162.31:8081/repository/maven-snapshots/</url>
 </snapshotRepository>
</distributionManagement>
#############################################################################
vi /usr/share/maven/conf/settings.xml
<server>
       <id>Snapshots</id>
       <username>admin</username>
       <password>admin123</password>
</server>

###########################################################################
This command is use for creating java sample project
mvn archetype:generate -DgroupId=atmecs.com -DartifactId=mysample -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
