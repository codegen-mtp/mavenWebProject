# Sample Maven Web Project

A Java Servlet web application packaged as a WAR file.

## Requirements
- JDK 21
- Apache Maven 3.9+
- Apache Tomcat 10.1+ (to run the web application)

## Build
Run this from the project root:

```bash
mvn clean package
```

The WAR file is created at `target/SampleMavenWebProject.war`.

## Deploy to Tomcat
1. Copy the WAR file into Tomcat's `webapps` folder.
2. Start Tomcat.
3. Visit `http://localhost:8080/SampleMavenWebProject/`.
4. Visit `http://localhost:8080/SampleMavenWebProject/hello` for the servlet page.

This uses Jakarta Servlet 6.0 and requires Tomcat 10.1 or newer.

## Jenkins
The included Jenkinsfile is for a Windows Jenkins agent and runs `mvn clean package` using `bat`. For Linux agents, replace `bat` with `sh`.
