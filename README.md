# About
An example Spring Cloud Config server that can read config data from a .yml or.properties file in a publicly hosted Git repo. The Git repo URI is set in this project's `application.properties`. This example uses a public GitHub repo but Spring Cloud Config should work with other platforms such as CodeCommit.

# Prerequisites
1. Install JDK 15.

# Getting Started
1. Create a public GitHub repository with an `application.yml` or `application.properties` file.
2. Clone your newly created repo, add some configuration data to your `application.yml` or `application.properties`, and push your changes back up.   
2. Import this project into an IDE such as an IntelliJ or gradle build it from the command line using `./gradlew build`.
3. Set the URI to your config repository in the `application.properties` file. Your config repository should also have an `application.properties` or `application.yml`.You may replace `application.properties` with an `application.yml` in either of your repos if you wish.
4. Run this Spring Boot application using `./gradlew bootRun` from the project root or using your IDE to run `SpringCloudConfigServerApplication.main`.
5. Go to [http://localhost:8001/spring-cloud-config-server/default/](`http://localhost:8001/spring-cloud-config-server/default/`). You should see a JSON result containing the properties from the file in your Git repo.
6. NOTE: You can also use another platform like CodeCommit, but that requires additional configuration in this project.

# Resources

https://cloud.spring.io/spring-cloud-config/multi/multi__spring_cloud_config_server.html
https://cloud.spring.io/spring-cloud-static/spring-cloud-config/2.2.1.RELEASE/reference/html/

