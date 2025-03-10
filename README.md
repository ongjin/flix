# Streaming Service

Spring Boot 기반 스트리밍 서비스 예제 프로젝트입니다.

## 주요 기능

-   REST API (예: 헬스체크)
-   PostgreSQL, Redis, Kafka 연동
-   Docker 컨테이너화

## 빌드 및 실행

1.  프로젝트 빌드:
    ```bash
    mvn clean package
    docker build -t streaming-service .
    docker run -p 8050:8050 streaming-service
    ```

---

## 5. pom.xml

<?xml version="1.0" encoding="UTF-8"?>

<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
<modelVersion>4.0.0</modelVersion>
<parent>
<groupId>org.springframework.boot</groupId>
<artifactId>spring-boot-starter-parent</artifactId>
<version>3.4.3</version>
<relativePath/> <!-- lookup parent from repository -->
</parent>
<groupId>com.zerry</groupId>
<artifactId>streaming-service</artifactId>
<version>0.0.1-SNAPSHOT</version>
<name>streaming-service</name>
<description>CYJ-streaming-service</description>
<url/>
<licenses>
<license/>
</licenses>
<developers>
<developer/>
</developers>
<scm>
<connection/>
<developerConnection/>
<tag/>
<url/>
</scm>
<properties>
<java.version>17</java.version>
</properties>
<dependencies>
<dependency>
<groupId>org.springframework.boot</groupId>
<artifactId>spring-boot-starter-actuator</artifactId>
</dependency>
<dependency>
<groupId>org.springframework.boot</groupId>
<artifactId>spring-boot-starter-data-jpa</artifactId>
</dependency>
<dependency>
<groupId>org.springframework.boot</groupId>
<artifactId>spring-boot-starter-data-redis</artifactId>
</dependency>
<dependency>
<groupId>org.springframework.boot</groupId>
<artifactId>spring-boot-starter-security</artifactId>
</dependency>
<dependency>
<groupId>org.springframework.boot</groupId>
<artifactId>spring-boot-starter-web</artifactId>
</dependency>
<dependency>
<groupId>org.springframework.kafka</groupId>
<artifactId>spring-kafka</artifactId>
</dependency>
<dependency>
<groupId>org.postgresql</groupId>
<artifactId>postgresql</artifactId>
<scope>runtime</scope>
</dependency>
<dependency>
<groupId>org.projectlombok</groupId>
<artifactId>lombok</artifactId>
<optional>true</optional>
</dependency>
<dependency>
<groupId>org.springframework.boot</groupId>
<artifactId>spring-boot-starter-test</artifactId>
<scope>test</scope>
</dependency>
<dependency>
<groupId>org.springframework.kafka</groupId>
<artifactId>spring-kafka-test</artifactId>
<scope>test</scope>
</dependency>
<dependency>
<groupId>org.springframework.security</groupId>
<artifactId>spring-security-test</artifactId>
<scope>test</scope>
</dependency>
<dependency>
<groupId>org.springframework.boot</groupId>
<artifactId>spring-boot-devtools</artifactId>
<optional>true</optional>
</dependency>
</dependencies>

    <build>
    	<plugins>
    		<plugin>
    			<groupId>org.apache.maven.plugins</groupId>
    			<artifactId>maven-compiler-plugin</artifactId>
    			<configuration>
    				<annotationProcessorPaths>
    					<path>
    						<groupId>org.projectlombok</groupId>
    						<artifactId>lombok</artifactId>
    					</path>
    				</annotationProcessorPaths>
    			</configuration>
    		</plugin>
    		<plugin>
    			<groupId>org.springframework.boot</groupId>
    			<artifactId>spring-boot-maven-plugin</artifactId>
    			<configuration>
    				<excludes>
    					<exclude>
    						<groupId>org.projectlombok</groupId>
    						<artifactId>lombok</artifactId>
    					</exclude>
    				</excludes>
    			</configuration>
    		</plugin>
    	</plugins>
    </build>

</project>

```

```
