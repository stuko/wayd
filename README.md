# token
* 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

# wayd

* git clone https://github.com/stuko/wayd.git
* git clone https://github.com/stuko/wayd-boot.git
* git clone https://github.com/stuko/wayd-new-base.git
* git clone https://github.com/stuko/wayd-new-containermanager.git
* git clone https://github.com/stuko/wayd-new-threadmanager.git
* git clone https://github.com/stuko/wayd-new-systemmanager.git
* git clone https://github.com/stuko/wayd-new-profilemanager.git
* git clone https://github.com/stuko/wayd-new-monitormanager.git
* git clone https://github.com/stuko/wayd-new-lockmanager.git
* git clone https://github.com/stuko/wayd-new-gcm.git
* git clone https://github.com/stuko/wayd-new-enginemanager.git
* git clone https://github.com/stuko/wayd-new-configmanager.git
* git clone https://github.com/stuko/wayd-meta-inf.git
* git clone https://github.com/stuko/wayd-new-3tyenginemanager.git

--> git clone https://github.com/stuko/XXXXXXXXXXXX.git
```
or
mvn clean deploy -DrepositoryId=internal.repo
   and
  <distributionManagement>   
    <repository>
      <id>internal.repo</id>
      <name>Project Release</name>
      <url>file://${project.basedir}/../wayd/release</url>
    </repository>
    <snapshotRepository>
      <uniqueVersion>true</uniqueVersion>
      <id>snapshot.repo</id>
      <name>Project Snapshots</name>
      <url>file://${project.basedir}/../wayd/snapshots</url>
    </snapshotRepository>
  </distributionManagement>  
```

* You must add repository and use depencency
```
<repository>
	<id>wayd</id>
	<url>https://github.com/stuko/wayd/raw/master/release</url>
	<snapshots>
		<enabled>true</enabled>
		<updatePolicy>always</updatePolicy>
	</snapshots>
</repository>
```

```
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-boot</artifactId>
			<version>0.0.1</version>
		</dependency>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-new-base</artifactId>
			<version>0.0.1</version>
		</dependency>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-new-containermanager</artifactId>
			<version>0.0.1</version>
		</dependency>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-meta-inf</artifactId>
			<version>0.0.1</version>
		</dependency>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-new-threadmanager</artifactId>
			<version>0.0.1</version>
		</dependency>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-new-systemmanager</artifactId>
			<version>0.0.1</version>
		</dependency>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-new-profilemanager</artifactId>
			<version>0.0.1</version>
		</dependency>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-new-monitormanager</artifactId>
			<version>0.0.1</version>
		</dependency>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-new-lockmanager</artifactId>
			<version>0.0.1</version>
		</dependency>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-new-enginemanager</artifactId>
			<version>0.0.1</version>
		</dependency>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-new-configmanager</artifactId>
			<version>0.0.1</version>
		</dependency>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-new-3tyenginemanager</artifactId>
			<version>0.0.1</version>
		</dependency>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-new-gcm</artifactId>
			<version>0.0.1</version>
		</dependency>
```

* Maven sample
```
<project xmlns="http://maven.apache.org/POM/4.0.0"
	xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
	<modelVersion>4.0.0</modelVersion>
	<groupId>com.stuko.wayd.container</groupId>
	<artifactId>wayd-new-container-XXXXXXXXX</artifactId>
	<version>XXXXXXXX</version>
	<properties>
		<project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
		<jdk.version>1.8</jdk.version>
    <project.basedir>./</project.basedir>
	  <project.build.directory>./target</project.build.directory>
		<project.root.target>./target</project.root.target>
		<project.build.final.target>./target</project.build.final.target>
		<maven.compiler.source>1.8</maven.compiler.source>
		<maven.compiler.target>1.8</maven.compiler.target>
		<maven.test.skip>true</maven.test.skip>
		<project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
		<shadedClassifier>bin</shadedClassifier>
		<java.version>1.8</java.version>
	</properties>


	<repositories>
		<repository>
			<id>sample-repository</id>
			<name>local repository</name>
			<url>file://${project.basedir}/lib</url>
		</repository>
		<repository>
			<id>wayd</id>
			<name>wayd-repository</name>
			<url>https://github.com/stuko/wayd/tree/master/release</url>
			<snapshots>
				<enabled>true</enabled>
				<updatePolicy>always</updatePolicy>
			</snapshots>
		</repository>
	</repositories>


	<build>
		<plugins>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-antrun-plugin</artifactId>
				<version>1.8</version>
				<executions>
					<execution>
						<phase>post-clean</phase>
						<goals>
							<goal>run</goal>
						</goals>
						<configuration>
							<tasks>
								<delete file="${project.build.directory}/lib/*.jar" />
							</tasks>
						</configuration>
					</execution>
				</executions>
			</plugin>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-jar-plugin</artifactId>
				<configuration>
					<archive>
						<manifest>
							<mainClass>com.stuko.kronos.BootLoader</mainClass>
						</manifest>
					</archive>
				</configuration>
			</plugin>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-dependency-plugin</artifactId>
				<executions>
					<execution>
						<id>copy-dependencies</id>
						<phase>package</phase>
						<goals>
							<goal>copy-dependencies</goal>
						</goals>
						<configuration>
							<outputDirectory>${project.build.directory}/lib</outputDirectory>
							<overWriteReleases>false</overWriteReleases>
							<overWriteSnapshots>false</overWriteSnapshots>
							<overWriteIfNewer>true</overWriteIfNewer>
						</configuration>
					</execution>
				</executions>
			</plugin>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-assembly-plugin</artifactId>
				<version>3.3.0</version>
				<configuration>
					<mainClass>com.stuko.kronos.BootLoader</mainClass>
					<descriptorRefs>
						<descriptorRef>jar-with-dependencies</descriptorRef>
					</descriptorRefs>
					<archive>
						<manifest>
							<addClasspath>true</addClasspath>
							<mainClass>com.stuko.kronos.BootLoader</mainClass>
						</manifest>
						<manifestEntries>
							<Class-Path>lib/</Class-Path>
						</manifestEntries>
					</archive>
				</configuration>
				<executions>
					<execution>
						<phase>package</phase>
						<goals>
							<goal>single</goal>
						</goals>
					</execution>
				</executions>
			</plugin>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-shade-plugin</artifactId>
				<executions>
					<execution>
						<phase>package</phase>
						<goals>
							<goal>shade</goal>
						</goals>
						<configuration>
							<shadedArtifactAttached>true</shadedArtifactAttached>
						</configuration>
					</execution>
				</executions>
			</plugin>
		</plugins>
	</build>

	<dependencies>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-boot</artifactId>
			<version>0.0.1</version>
		</dependency>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-new-base</artifactId>
			<version>0.0.1</version>
		</dependency>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-new-containermanager</artifactId>
			<version>0.0.1</version>
		</dependency>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-meta-inf</artifactId>
			<version>0.0.1</version>
		</dependency>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-new-threadmanager</artifactId>
			<version>0.0.1</version>
		</dependency>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-new-systemmanager</artifactId>
			<version>0.0.1</version>
		</dependency>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-new-profilemanager</artifactId>
			<version>0.0.1</version>
		</dependency>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-new-monitormanager</artifactId>
			<version>0.0.1</version>
		</dependency>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-new-lockmanager</artifactId>
			<version>0.0.1</version>
		</dependency>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-new-enginemanager</artifactId>
			<version>0.0.1</version>
		</dependency>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-new-configmanager</artifactId>
			<version>0.0.1</version>
		</dependency>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-new-3tyenginemanager</artifactId>
			<version>0.0.1</version>
		</dependency>
		<dependency>
			<groupId>com.stuko.wayd</groupId>
			<artifactId>wayd-new-gcm</artifactId>
			<version>0.0.1</version>
		</dependency>
	
	</dependencies>

</project>
```

```
mvn -DaltDeploymentRepository=snapshot::default::file:../wayd/snapshots clean deploy

###################################
# wayd boot copy in W2K
###################################
copy /Y ..\wayd-boot\target\*.jar .\

###################################
# wayd library copy in W2K
###################################
mkdir wayd-lib
copy /Y ..\wayd-new-base\target\*.jar .\wayd-lib\
copy /Y ..\wayd-new-configmanager\target\*.jar .\wayd-lib\
copy /Y ..\wayd-new-containermanager\target\*.jar .\wayd-lib\
copy /Y ..\wayd-new-gcm\target\*.jar .\wayd-lib\
copy /Y ..\wayd-new-systemmanager\target\*.jar .\wayd-lib\
copy /Y ..\wayd-new-enginemanager\target\*.jar .\wayd-lib\
copy /Y ..\wayd-new-lockmanager\target\*.jar .\wayd-lib\
copy /Y ..\wayd-new-threadmanager\target\*.jar .\wayd-lib\
copy /Y ..\wayd-new-monitormanager\target\*.jar .\wayd-lib\
copy /Y ..\wayd-new-profilemanager\target\*.jar .\wayd-lib\
copy /Y ..\wayd-new-3tyenginemanager\target\*.jar .\wayd-lib\

mkdir dependency-lib
copy /Y ..\wayd-new-base\target\lib\*.jar .\dependency-lib\
copy /Y ..\wayd-new-configmanager\target\lib\*.jar .\dependency-lib\
copy /Y ..\wayd-new-containermanager\target\lib\*.jar .\dependency-lib\
copy /Y ..\wayd-new-gcm\target\lib\*.jar .\dependency-lib\
copy /Y ..\wayd-new-systemmanager\target\lib\*.jar .\dependency-lib\
copy /Y ..\wayd-new-enginemanager\target\lib\*.jar .\dependency-lib\
copy /Y ..\wayd-new-lockmanager\target\lib\*.jar .\dependency-lib\
copy /Y ..\wayd-new-threadmanager\target\lib\*.jar .\dependency-lib\
copy /Y ..\wayd-new-monitormanager\target\lib\*.jar .\dependency-lib\
copy /Y ..\wayd-new-profilemanager\target\lib\*.jar .\dependency-lib\
copy /Y ..\wayd-new-3tyenginemanager\target\lib\*.jar .\dependency-lib\


###################################
# wayd boot copy in W2K
###################################
cp -rf ../wayd-boot/target/*.jar ./

###################################
# wayd library copy in LINUX
###################################
mkdir wayd-lib
cp -rf ../wayd-new-base/target/*.jar ./wayd-lib/
cp -rf ../wayd-new-configmanager/target/*.jar ./wayd-lib/
cp -rf ../wayd-new-containermanager/target/*.jar ./wayd-lib/
cp -rf ../wayd-new-gcm/target/*.jar ./wayd-lib/
cp -rf ../wayd-new-systemmanager/target/*.jar ./wayd-lib/
cp -rf ../wayd-new-enginemanager/target/*.jar ./wayd-lib/
cp -rf ../wayd-new-lockmanager/target/*.jar ./wayd-lib/
cp -rf ../wayd-new-threadmanager/target/*.jar ./wayd-lib/
cp -rf ../wayd-new-monitoringmanager/target/*.jar ./wayd-lib/
cp -rf ../wayd-new-profilemanager/target/*.jar ./wayd-lib/
cp -rf ../wayd-new-3tyenginemanager/target/*.jar ./wayd-lib/

mkdir dependency-lib
cp -rf ../wayd-new-base/target/lib/*.jar ./dependency-lib/
cp -rf ../wayd-new-configmanager/target/lib/*.jar ./dependency-lib/
cp -rf ../wayd-new-containermanager/target/lib/*.jar ./dependency-lib/
cp -rf ../wayd-new-gcm/target/lib/*.jar ./dependency-lib/
cp -rf ../wayd-new-systemmanager/target/lib/*.jar ./dependency-lib/
cp -rf ../wayd-new-enginemanager/target/lib/*.jar ./dependency-lib/
cp -rf ../wayd-new-lockmanager/target/lib/*.jar ./dependency-lib/
cp -rf ../wayd-new-threadmanager/target/lib/*.jar ./dependency-lib/
cp -rf ../wayd-new-monitoringmanager/target/lib/*.jar ./dependency-lib/
cp -rf ../wayd-new-profilemanager/target/lib/*.jar ./dependency-lib/
cp -rf ../wayd-new-3tyenginemanager/target/lib/*.jar ./dependency-lib/

```
