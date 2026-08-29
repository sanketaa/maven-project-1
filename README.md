# Java Maven Project — Earlier Course Snapshot

> This repository is an earlier learning snapshot and substantially duplicates [maven-project](https://github.com/sanketaa/maven-project). For the clearest documentation and portfolio reference, use the primary repository.

## Background

This code was created while following James Lee's Jenkins course. It is preserved to show an earlier stage of the Maven and continuous-integration exercises, not as a separate original application.

The repository demonstrates a basic Java multi-module Maven build:

- A parent POM coordinates the complete build.
- The `server` module packages Java logic as a JAR.
- The `webapp` module packages a JSP application as a WAR.
- JUnit and Hamcrest tests validate a small greeting class.
- Maven reporting plugins support code-quality and test reports.
- The structure can be used to practice Jenkins build jobs.

## Structure

```text
.
├── pom.xml
├── server
│   ├── pom.xml
│   └── src
│       ├── main/java/com/example/Greeter.java
│       └── test/java/com/example/TestGreeter.java
└── webapp
    ├── pom.xml
    └── src/main/webapp
        ├── index.jsp
        └── WEB-INF/web.xml
```

## Build

This project uses Java 6-era compiler settings and historical Maven plugins. A compatible older JDK may be required.

```bash
mvn clean package
mvn test
mvn site
```

The build produces a server JAR and a web application WAR.

## Difference from the Primary Repository

Most files match the primary `maven-project` repository. In this snapshot, `Greeter.java` contains an unfinished Javadoc TODO and uses a non-final method signature. These differences represent an earlier point in the course exercise rather than a distinct project.

## Portfolio Note

This repository is kept for learning-history purposes. The primary [maven-project](https://github.com/sanketaa/maven-project) repository has the complete project explanation, architecture, commands, limitations, and modernization ideas.

## Attribution

The starting source code is associated with James Lee's Jenkins course. This repository does not claim the course example as wholly original work.
