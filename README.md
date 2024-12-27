## Java Application with Jenkins Pipeline

This project demonstrates a simple Java application with automated CI/CD using Jenkins pipeline and Slack notifications.

### Project Structure
```
├── src/
│   ├── main/
│   │   └── java/
│   │       └── com/
│   │           └── example/
│   │               ├── App.java
│   │               └── Calculator.java
│   └── test/
│       └── java/
│           └── com/
│               └── example/
│                   └── CalculatorTest.java
├── Jenkinsfile
├── pom.xml
└── README.md
```

### Prerequisites
- Java 11 or higher
- Maven 3.6+
- Jenkins with following plugins:
  - Pipeline
  - Maven Integration
  - JUnit
  - Slack Notification
- Slack workspace with webhook configured

### Setup Instructions

1. Configure Jenkins:
   - Install required plugins
   - Add Maven tool in Jenkins Global Tool Configuration
   - Configure Slack notification plugin with workspace webhook

2. Create Jenkins Pipeline:
   - Create new Pipeline job
   - Configure SCM to point to your repository
   - Use the Jenkinsfile from this repository

3. Build locally:
```bash
mvn clean install
```

4. Run tests:
```bash
mvn test
```

### Features
- Basic calculator operations
- Unit tests with JUnit
- Automated build pipeline
- Code quality checks
- Slack notifications for build status