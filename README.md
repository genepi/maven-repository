# genepi-libs Maven Repository

This repo hosts all artifacts. 
Currently it includes three libraries (genepi-hadoop; genepi-io; genepi-db) which are used in many of our projects. All artifacts are located in the mvn-repo branch

## Usage

- Add this to your repository part in your pom.xml:

		<myxml>
		<repository>
			<id>genepi</id>
			<url>https://raw.github.com/genepi/maven-repository/mvn-repo/</url>
			<snapshots>
				<enabled>true</enabled>
				<updatePolicy>always</updatePolicy>
			</snapshots>
		</repository>


- Add this to your dependencies part in your pom.xml:
		
		<myxml>
		<dependency>
			<groupId>genepi</groupId>
			<artifactId>genepi-io</artifactId>
			<version>1.0.2</version>
		</dependency>
		<!-- for usage with Apache YARN, otherwise use "mr1-1.1.1" for version tag -->
		<dependency>
			<groupId>genepi</groupId>
			<artifactId>genepi-hadoop</artifactId>
			<version>yarn-1.1.0</version>
		</dependency>
		</myxml>
