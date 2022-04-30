# core-store
collector, for all products with price and resellers value
This XML file does not appear to have any style information associated with it. The document tree is shown below.
<project>
 <!--  model version - always 4.0.0 for Maven 2.x POMs  -->
<modelVersion>4.0.0</modelVersion>
 <!--
 project coordinates - values which uniquely identify this project 
-->
<groupId>com.stripe.sample</groupId>
<artifactId>stripe-checkout</artifactId>
<version>1.0.0-SNAPSHOT</version>
 <!--  library dependencies  -->
<dependencies>
<dependency>
<groupId>org.slf4j</groupId>
<artifactId>slf4j-simple</artifactId>
<version>1.7.21</version>
</dependency>
<dependency>
<groupId>com.sparkjava</groupId>
<artifactId>spark-core</artifactId>
<version>2.8.0</version>
</dependency>
<dependency>
<groupId>com.google.code.gson</groupId>
<artifactId>gson</artifactId>
<version>2.3.1</version>
</dependency>
<dependency>
<groupId>org.projectlombok</groupId>
<artifactId>lombok</artifactId>
<version>1.18.8</version>
<scope>provided</scope>
</dependency>
<dependency>
<groupId>com.stripe</groupId>
<artifactId>stripe-java</artifactId>
<version>19.45.0</version>
</dependency>
</dependencies>
<build>
<sourceDirectory>${project.basedir}</sourceDirectory>
<plugins>
<plugin>
<groupId>org.apache.maven.plugins</groupId>
<artifactId>maven-compiler-plugin</artifactId>
<version>2.3.2</version>
<configuration>
<source>1.8</source>
<target>1.8</target>
</configuration>
</plugin>
<plugin>
<artifactId>maven-assembly-plugin</artifactId>
<executions>
<execution>
<phase>package</phase>
<goals>
<goal>single</goal>
</goals>
</execution>
</executions>
<configuration>
<descriptorRefs>
 <!--  This tells Maven to include all dependencies  -->
<descriptorRef>jar-with-dependencies</descriptorRef>
</descriptorRefs>
<archive>
<manifest>
<mainClass>Server</mainClass>
</manifest>
</archive>
</configuration>
</plugin>
</plugins>
</build>
</project>
