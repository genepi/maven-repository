# Our local maven repository

This repo hosts all artifacts. 
Currently it includes two libraries (genepi-hadoop; genepi-io) which are used in many of our projects. All artifacts are located in the mvn-repo branch

## Usage

- Add this to your repository part in your pom.xml:

		<myxml>
		<repository>
			<id>genepi-hadoop</id>
			<url>https://raw.github.com/genepi/maven-repository/mvn-repo/</url>
			<snapshots>
				<enabled>true</enabled>
				<updatePolicy>always</updatePolicy>
			</snapshots>
		</repository>


		<repository>
			<id>genepi-io</id>
			<url>https://raw.github.com/genepi/maven-repository/genepi-io</url>
			<snapshots>
				<enabled>true</enabled>
				<updatePolicy>always</updatePolicy>
			</snapshots>
		</repository>
		</myxml>
		
- Add this to your dependencies part in your pom.xml:
		
		<myxml>
		<dependency>
			<groupId>genepi</groupId>
			<artifactId>genepi-io</artifactId>
			<version>1.0</version>
		</dependency>
		<!--for Apache YARN -->
		<dependency>
			<groupId>genepi</groupId>
			<artifactId>genepi-hadoop</artifactId>
			<version>yarn-1.0</version>
		</dependency>
		</myxml>
