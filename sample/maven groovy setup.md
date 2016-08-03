```xml
	<build> <!-- Maven compilier 設定 -->
		<plugins>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-compiler-plugin</artifactId> <!-- http://maven.apache.org/plugins/maven-compiler-plugin/index.html -->
				<version>3.3</version>
				<configuration>
					<source>${java-version}</source>
					<target>${java-version}</target>
					<!-- Add groovy source compiler -->
					<compilerId>groovy-eclipse-compiler</compilerId>
					<verbose>true</verbose>
					<fork>true</fork>
					<compilerArguments>
						<javaAgentClass>lombok.launch.Agent</javaAgentClass>
					</compilerArguments>

				</configuration>
				<dependencies> <!-- Add groovy source compiler -->
					<dependency>
						<groupId>org.codehaus.groovy</groupId>
						<artifactId>groovy-eclipse-compiler</artifactId> <!-- https://github.com/groovy/groovy-eclipse/wiki/Groovy-Eclipse-Maven-plugin -->
						<version>2.9.2-01</version>
					</dependency>
					<dependency>
						<groupId>org.codehaus.groovy</groupId>
						<artifactId>groovy-eclipse-batch</artifactId>
						<version>2.4.3-01</version>
					</dependency>
					<dependency>
						<groupId>org.projectlombok</groupId>
						<artifactId>lombok</artifactId>
						<version>${lombok-version}</version>
					</dependency>
				</dependencies>
			</plugin>

			<!-- https://github.com/groovy/groovy-eclipse/wiki/Groovy-Eclipse-Maven-plugin -->
			<plugin>
				<groupId>org.codehaus.groovy</groupId>
				<artifactId>groovy-eclipse-compiler</artifactId>
				<version>2.9.2-01</version>
				<extensions>true</extensions>
			</plugin>

			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-war-plugin</artifactId>	<!-- https://maven.apache.org/plugins/maven-war-plugin/ -->
				<version>2.6</version>
				<configuration>
					<failOnMissingWebXml>false</failOnMissingWebXml>
				</configuration>
			</plugin>

		</plugins>
	</build>
```
